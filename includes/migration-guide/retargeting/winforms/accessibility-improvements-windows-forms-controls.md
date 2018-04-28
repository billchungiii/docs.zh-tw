### <a name="accessibility-improvements-in-windows-forms-controls"></a>Windows Forms 控制項的協助工具改善

|   |   |
|---|---|
|詳細資料|Windows Forms 正在使用協助工具技術改善其運作方式，以便為 Windows Forms 客戶提供更好的支援。 這些包括下列變更：<ul><li>改善高對比模式期間之顯示方式的變更。</li><li>改善屬性瀏覽器體驗的變更。 屬性瀏覽器改善包括：</li><li>透過各種下拉式選取視窗進行更佳的鍵盤導覽。</li><li>減少不必要的定位停駐點。</li><li>更適當地報告控制項類型。</li><li>改善的朗讀程式行為。</li><li>在控制項中實作遺漏的 UI 協助工具模式的變更。</li></ul>|
|建議|<strong>如何選擇加入或退出這些變更</strong>為了讓應用程式可受益於這些變更，它必須在 .NET Framework 4.7.1 或更新版本上執行。 應用程式可以用下列任一種方式受益於這些變更：<ul><li>它已重新編譯為以 .NET Framework 4.7.1 為目標。 在以 .NET Framework 4.7.1 或更新版本為目標的 Windows Forms 應用程式上，預設會啟用這些協助工具變更。</li><li>藉由在 app config 檔案的 <code>&lt;runtime&gt;</code> 區段中新增下列 [AppContext 參數](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)，並將它設定為 <code>false</code>，選擇退出舊版協助工具行為，如下列範例所示。</li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>以 .NET Framework 4.7.1 或更新版本為目標，並且想要保留舊版協助工具行為的應用程式，可以藉由明確將此 AppContext 參數設為 <code>true</code>，選擇使用舊版的協助工具功能。如需 UI 自動化的概觀，請參閱 [UI 自動化概觀](~/docs/framework/ui-automation/ui-automation-overview.md)。<strong>已新增對 UI 自動化模式和屬性的支援</strong>協助工具用戶端可以藉由使用通用的公開描述叫用模式，來利用新的 WinForms 協助工具功能。 這些不是 WinForms 特有模式。 例如，協助工具用戶端可以在 IAccessible 介面 (MAAS) 上呼叫 QueryInterface 方法，以取得 IServiceProvider 介面。 如果此介面可供使用，用戶端可以使用其 QueryService 方法來要求 IAccessibleEx 介面。 如需詳細資訊，請參閱[從用戶端使用 IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561924.aspx)。 從.NET Framework 4.7.1，IServiceProvider 開始和[IAccessibleEx](https://msdn.microsoft.com/library/windows/desktop/dd561898.aspx) （如果適用的話） 可供 WinForms 協助工具物件。 .NET Framework 4.7.1 新增下列使用者介面自動化模式和屬性的支援：<ul><li><code>T:System.Windows.Forms.ToolStripSplitButton</code> 和 <code>T:System.Windows.Forms.ComboBox</code> 控制項支援[展開/摺疊模式](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md)。</li><li><code>T:System.Windows.Forms.ToolStripMenuItem</code> 控制項有 [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) 屬性值 <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>。</li><li><code>T:System.Windows.Forms.ToolStripItem</code> 控制項支援 [Name](xref:System.Windows.Automation.AutomationElement.NameProperty) 屬性和[展開/摺疊模式](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md)。</li><li><code>T:System.Windows.Forms.ToolStripDropDownItem</code> 控制項支援 <xref:System.Windows.Forms.AccessibleEvents>表示展開或摺疊下拉式清單時的 StateChange 和 NameChange。</li><li><code>T:System.Windows.Forms.ToolStripDropDownButton</code> 控制項具有 [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) 屬性值 <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType>。</li><li><code>T:System.Windows.Forms.DataGridViewCheckBoxCell</code> 控制項支援[切換模式](xref:System.Windows.Automation.TogglePattern)。</li><li><code>T:System.Windows.Forms.NumericUpDown</code> 和 <code>T:System.Windows.Forms.DomainUpDown</code> 控制項支援 [Name](xref:System.Windows.Automation.AutomationElement.NameProperty)，而且具有 [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-spinner-control-type.md) 值 <xref:System.Windows.Automation.ControlType.Spinner?displayProperty=nameWithType>。</li></ul><strong>對 PropertyGrid 控制項的改善</strong>.NET Framework 4.7.1 在 PropertyBrowser 控制項中新增下列改善：<ul><li>使用者在 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項中輸入不正確的值時所顯示之 [錯誤] 對話方塊中的 [詳細資料] 按鈕，支援[展開/摺疊模式](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md)、狀態與名稱變更通知，以及值為 <xref:System.Windows.Automation.ControlType.MenuItem?displayProperty=nameWithType> 的 [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) 屬性。</li><li>展開 [錯誤] 對話方塊的 [詳細資料] 按鈕時所顯示的 [訊息] 窗格，現在可透過鍵盤存取，並可讓朗讀程式宣告錯誤訊息的內容。</li><li><code>T:System.Windows.Forms.PropertyGrid</code> 控制項中資料列的 <xref:System.Windows.Forms.AccessibleRole> 已從 &quot;Row&quot; 變更為 &quot;Cell&quot;。 此資料格會對應至 UIA ControlType &quot;DataItem&quot;，讓它支援適當的鍵盤快速鍵和朗讀程式宣告。</li><li><code>T:System.Windows.Forms.PropertyGrid</code> 控制項將 <code>P:System.Windows.Forms.PropertySort</code> 屬性設定為 <code>F:System.Windows.Forms.PropertySory.Categorized</code> 時代表標頭項目的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項資料列，具有 [ControlType](~/docs/framework/ui-automation/ui-automation-support-for-the-menubar-control-type.md) 屬性值 <xref:System.Windows.Automation.ControlType.Button?displayProperty=nameWithType></li><li><code>T:System.Windows.Forms.PropertyGrid</code> 控制項將 <code>P:System.Windows.Forms.PropertySort</code> 屬性設定為 <code>F:System.Windows.Forms.PropertySory.Categorized</code> 時代表標頭項目的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項資料列，支援[展開/摺疊模式](~/docs/framework/ui-automation/implementing-the-ui-automation-expandcollapse-control-pattern.md)。</li><li>改善了方格與其上工具列之間的鍵盤導覽。 按下 &quot;Shift-Tab&quot; 現在會選取第一個工具列按鈕，而不是整個工具列</li><li>在高對比模式中顯示的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項，現在會圍繞對應於目前 <code>P:System.Windows.Forms.PropertySort</code> 屬性值的工具列按鈕繪製焦點矩形。</li><li>在高對比模式中顯示且 <code>P:System.Windows.Forms.PropertySort</code> 屬性設定為 <code>F:System.Windows.Forms.PropertySory.Categorized</code> 的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項，現在將以高對比的色彩顯示分類標頭的背景。</li><li><code>T:System.Windows.Forms.PropertyGrid</code> 控制項可以更好地區別具有焦點的工具列項目與表示 <code>P:System.Windows.Forms.PropertySort</code> 屬性目前值的工具列項目。 此修正包含高對比變更及非高對比案例的變更。</li><li>表示 <code>P:System.Windows.Forms.PropertySort</code> 屬性目前值的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項工具列項目支援[切換模式](xref:System.Windows.Automation.TogglePattern)。</li><li>改善了朗讀程式對區分對齊選擇器中所選取對齊方式的支援。</li><li>在表單上顯示空的 <code>T:System.Windows.Forms.PropertyGrid</code> 控制項時，它現在會接收焦點，而之前並不會。</li></ul><strong>使用高對比佈景主題中作業系統定義的色彩</strong><ul><li><code>P:System.Windows.Forms.Control.FlatStyle</code> 設定為 <xref:System.Windows.Forms.FlatStyle.System?displayProperty=nameWithType> (這是預設樣式) 的 <code>T:System.Windows.Forms.Button</code> 和 <code>T:System.Windows.Forms.CheckBox</code> 控制項，現在使用選取的高對比佈景主題中作業系統定義的色彩。 以往，文字和背景色彩不會呈現對比，因此難以閱讀。</li><li><code>P:System.Windows.Forms.Control.Enabled</code> 設定為 <em>false</em> 的 <code>T:System.Windows.Forms.Button</code>、<code>T:System.Windows.Forms.CheckBox</code>、<code>T:System.Windows.Forms.RadioButton</code>、<code>T:System.Windows.Forms.Label</code>、<code>T:System.Windows.Forms.LinkLabel</code> 和 <code>T:System.Windows.Forms.GroupBox</code>，使用了陰影色彩來呈現高對比佈景主題中的文字，導致與背景的對比過低。 現在，這些控制項使用作業系統所定義的「已停用文字」色彩。 此修正套用至 <code>P:System.Windows.Forms.Control.FlatStyle</code> 屬性設定為非 <code>F:System.Windows.Forms.FlatStyle.System</code> 值的控制項。 後者的控制項是由作業系統呈現。</li><li><code>T:System.Windows.Forms.DataGridView</code> 現在會於目前焦點所在的儲存格內容周圍呈現可見的矩形。 之前，這不會顯示在特定的高對比佈景主題中。</li><li><code>P:System.Windows.Forms.ToolStripItem.Enabled</code> 屬性設定為 <em>false</em> 的 <code>T:System.Windows.Forms.ToolStripMenuItem</code> 控制項，現在使用作業系統所定義的「已停用文字」色彩。</li><li><code>P:System.Windows.Forms.ToolStripItem.Checked</code> 屬性設定為 <em>true</em> 的 <code>T:System.Windows.Forms.ToolStripMenuItem</code> 控制項，現在以對比的系統色彩呈現相關聯的核取記號。  先前的核取記號色彩對比不足，無法在高對比佈景主題中顯示。</li></ul>注意：Windows 10 已變更某些高對比系統色彩的值。 Windows Forms 架構是以 Win32 架構為基礎。 為獲得最佳體驗、在最新版的 Windows 上執行，以及新增最新作業系統變更，請在測試應用程式中新增 app.manifest 檔案，並取消註解下列程式碼：<pre><code>&lt;!-- Windows 10 --&gt;&#13;&#10;&lt;supportedOS Id=&quot;{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}&quot; /&gt;&#13;&#10;</code></pre><strong>改善的鍵盤導覽</strong><ul><li>當 <code>T:System.Windows.Forms.ComboBox</code> 控制項將 <code>P:System.Windows.Forms.ComboBox.DropDownStyle</code> 設定為 <code>F:System.Windows.Forms.DropDownStyle.DropDownList</code>，且它是表單中定位順序的第一個控制項時，如果使用鍵盤來開啟父表單，它現在會顯示焦點矩形。 在這項變更之前，鍵盤焦點是在這個控制項上，但不會呈現焦點指標。</li></ul><strong>改善的朗讀程式支援</strong><ul><li><code>T:System.Windows.Forms.MonthCalendar</code> 控制項已針對輔助技術新增存取控制項的支援，包括讓朗讀程式可以讀取先前無法讀取的控制項值。</li><li><code>T:System.Windows.Forms.CheckedListBox</code> 控制項現在會於 <code>P:System.Windows.Forms.CheckState</code> 屬性已變更時通知 [朗讀程式]。 之前，朗讀程式不會收到通知，因此使用者不會被告知 <code>P:System.Windows.Forms.CheckState</code> 已更新。</li><li><code>T:System.Windows.Forms.LinkLabel</code> 控制項已變更其告知朗讀程式有關控制項文字的方式。 之前，朗讀程式會宣告這段文字兩次，並將 &quot;&amp;&quot; 符號讀取為實際文字，即使使用者看不到這些文字也一樣。 已從朗讀程式宣告中移除重複的文字，以及不必要的 &quot;&amp;&quot; 符號。</li><li><code>T:System.Windows.Forms.DataGridViewCell</code> 控制項類型現在會正確地向朗讀程式和其他輔助技術報告唯讀狀態。</li><li>朗讀程式現在可以讀取[多重文件介面](~/docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md)應用程式中子視窗的系統功能表。</li><li>朗讀程式現在可以讀取 <code>P:System.Windows.Forms.ToolStripItem.Enabled</code> 屬性設定為 <em>false</em> 的 <code>T:System.Windows.Forms.ToolStripMenuItem</code> 控制項。 之前，朗讀程式無法將焦點放在已停用的功能表項目來讀取內容。</li></ul>|
|範圍|主要|
|版本|4.7.1|
|類型|正在重定目標|
|受影響的 API|<ul><li><xref:System.Windows.Forms.ToolStripDropDownButton.CreateAccessibilityInstance?displayProperty=nameWithType></li><li><xref:System.Windows.Forms.DomainUpDown.DomainUpDownAccessibleObject.Name?displayProperty=nameWithType></li><li>[MonthCalendar.AccessibilityObject](xref:System.Windows.Forms.Control.AccessibilityObject)</li></ul>|
