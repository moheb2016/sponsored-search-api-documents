# ReportDefinition
ReportDefinitionオブジェクトは、レポート定義を表します。
### Service
+ [ReportDefinitionService](../../services/ReportDefinitionService.md)

### Namespace
[ReportDefinitionService#Namespace](../../services/ReportDefinitionService.md#namespace)

<table>
 <tr>
  <th>Field</th>
  <th>Type</th>
  <th>Description</th>
  <th>response</th>
  <th>get</th>
  <th>add</th>
  <th>set</th>
  <th>remove</th>
 </tr>
 <tr>
  <td>accountId</td>
  <td>xsd:long</td>
  <td>アカウントIDです。</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>reportId</td>
  <td>xsd:long</td>
  <td>レポートIDです。</td>
  <td>yes</td>
  <td>-</td>
  <td>-</td>
  <td>-</td>
  <td>Requirement</td>
 </tr>
 <tr>
  <td>reportName</td>
  <td>xsd:string</td>
  <td>レポート名です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>reportType</td>
  <td>enum <a href="ReportType.md">ReportType</a></td>
  <td>レポートの種類です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>dateRangeType</td>
  <td>enum <br><a href="ReportDateRangeType.md">ReportDateRangeType</a></td>
  <td>レポートの集計対象期間です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>dateRange</td>
  <td><a href="ReportDateRange.md">DateRange</a></td>
  <td>ユーザーにより設定されるレポート集計の範囲期間です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>fields[1...100]</td>
  <td>xsd:string</td>
  <td>フィールド（レポートの出力項目名）です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Requirement</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>sortFields[0...1]</td>
  <td><a href="ReportSortField.md">ReportSortField</a></td>
  <td>フィールド名を指定し、ソートします。</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>filters[0...6]</td>
  <td><a href="ReportFilter.md">ReportFilter</a></td>
  <td>レポートのフィルタ条件です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>isTemplate</td>
  <td>enum <br><a href="ReportIsTemplate.md">ReportIsTemplate</a></td>
  <td>レポートテンプレートに登録するかを選択します。<br>※Default：FALSE（登録しない）</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>intervalType</td>
  <td>enum <br><a href="ReportIntervalType.md">ReportIntervalType</a></td>
  <td>定期レポート作成タイミング設定です。<br>※Default：ONETIME</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>specifyDay</td>
  <td>xsd:int</td>
  <td>定期レポート作成日の設定です。<br>※1～31の日付を指定できます。<br>※毎月初は「1」、毎月末は「31」と指定してください。<br>※intervalType：SPECIFYDAYの場合のみ有効です。</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>format</td>
  <td>enum <br><a href="ReportDownloadFormat.md">ReportDownloadFormat</a></td>
  <td>ダウンロードレポートのファイル形式です。<br>※Default：CSV</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>encode</td>
  <td>enum <br><a href="ReportDownloadEncode.md">ReportDownloadEncode</a></td>
  <td>ダウンロードレポートの文字コードです。<br>※Default：UTF-8</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>language</td>
  <td>enum <br><a href="ReportLanguage.md">ReportLanguage</a></td>
  <td>レポートの出力言語です。<br>※Default：JA（日本語）</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>compress</td>
  <td>enum <br><a href="ReportCompressType.md">ReportCompressType</a></td>
  <td>レポートを圧縮して出力するかを選択します。<br>※Default：NONE（圧縮しない）</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>includeZeroImpressions</td>
  <td>enum <br><a href="ReportIncludeZeroImpressions.md">ReportIncludeZeroImpressions</a></td>
  <td>0インプレッションの行をレポートに含めるかを選択します。<br>※Default：FALSE（含めない）</td>
  <td>yes</td>
  <td>-</td>
  <td>Optional</td>
  <td>-</td>
  <td>-</td>
 </tr>
 <tr>
  <td>includeDeleted</td>
  <td>enum <br><a href="ReportIncludeDeleted.md">ReportIncludeDeleted</a></td>
  <td>削除済みの項目を出力対象にするかを選択します。<br>
  FALSEを指定した場合は、削除済み、および掲載停止の項目が出力対象外になります。<br>
  ※Default：TRUE（出力対象）<br>
  </td>
  <td>yes</td>
  <td>-</td>
  <td>Optional<br>※レポートタイプが以下の場合のみ。<br>・CAMPAIGN<br>・ADGROUP<br>・AD<br>・KEYWORDS<br>・FEED_ITEM<br>・AD_CUSTOMIZERS<br>これ以外の場合はIgnore
</td>
  <td>-</td>
  <td>-</td>
 </tr>
</table>

<a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nd/2.1/jp/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by-nd/2.1/jp/">クリエイティブ・コモンズ 表示 - 改変禁止 2.1 日本 ライセンスの下に提供されています。</a>