<div class="col-md-2">
    <label class="form-label">Zip Code:<span class="RequiredSymbol">*</span></label>
</div>
<div class="col-md-2">
    <asp:TextBox ID="txtZipCode" runat="server" CssClass="form-control" MaxLength="6"></asp:TextBox>
    <asp:RequiredFieldValidator ID="rfvtxtZipCode" ControlToValidate="txtZipCode" runat="server" ErrorMessage="*Required" Display="Dynamic" CssClass="error" SetFocusOnError="true"   ValidationGroup="SaveVendor"></asp:RequiredFieldValidator>
    <asp:RegularExpressionValidator ID="rgvtxtZipCode" runat="server" ControlToValidate="txtZipCode" ValidationExpression="^[0-9]{6}$" Display="Dynamic" CssClass="error" SetFocusOnError="true"   ValidationGroup="SaveVendor" ErrorMessage="*Zip code length should be 6 digits..!!"></asp:RegularExpressionValidator>
    <%--<asp:CustomValidator ID="CVtxtZipCode" ControlToValidate="txtZipCode" runat="server" ValidateEmptyText="true" ErrorMessage="*Required" Display="Static" CssClass="error" ClientIDMode="Static" ClientValidationFunction="Validate_panNo" ValidationGroup="SaveVendor"></asp:CustomValidator>--%>
    <ajax:FilteredTextBoxExtender ID="fltPinCode" TargetControlID="txtZipCode" FilterMode="ValidChars" FilterType="Numbers" runat="server"></ajax:FilteredTextBoxExtender>
</div>
