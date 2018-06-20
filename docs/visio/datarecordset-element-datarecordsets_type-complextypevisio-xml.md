---
title: データ レコード セットの要素 (DataRecordSets_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805170"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>データ レコード セットの要素 (DataRecordSets_Type complexType)'Visio XML (')

Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |ドキュメント内にある**データ レコード セット**のすべての要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |ADO レコード セットの ADO 標準 XML スキーマに適合して、データ レコード セット内のデータを説明する、XML が含まれています。  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |前回成功した自動リンクで実行されたアクション ユーザー インターフェイスからの図形データ項目の親**データ レコード セット**の要素内の列を比較するルールを定義します。  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データ列が Visio ユーザー インターフェイスの [**外部データ**] ウィンドウで表示する方法を定義し、そのデータ型を定義して、書式設定、列のデータが適用されます。  <br/> |
|[Datacolumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データ レコード セット内のすべての**列**要素が含まれています。  <br/> |
|[主キー](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |データ レコード セット内の 1 つまたは複数の主キー列を識別します。  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |データ レコード セットが更新された後に、競合がある図形にリンクされているデータ レコード セット内の行を示します。  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |レコード セットのデータ行を図形にマップします。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|チェックサム  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |チェックサムの値は、Visio によって生成され、データ レコード セットのプロパティに基づきます。 この attirbute を 0 に設定します。Visio には、実行時にこの値が再計算されます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|コマンド  <br/> |xsd:string  <br/> |省略可能  <br/> |コマンド文字列は、データ ソースからデータのクエリを使用します。  <br/> |Xsd:string の値を入力します。  <br/> |
|接続 Id  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |関連付けられた**DataConnection**オブジェクトの接続の ID です。 XML データ ソースが存在しません。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |データ レコード セット ID、ドキュメント内で一意です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |表示、わかりやすい) データ レコード セットの名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |次利用可能な Visio の行 id。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|選択肢  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |データ レコード セットに適用するオプションです。 使用可能な値は、次の表に示すようにそれらの 1 つ以上の任意の組み合わせにできます。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|間隔  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |頻度 (分単位) では、Visio は、データ レコード セットを自動的に更新します。 この値は、1 以上にする必要があります。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |省略可能  <br/> |かどうかデータ調整のユーザー インターフェイスを無効にする必要があります。 True (1 を) では、ユーザー インターフェイス (UI) を無効にします。 UI を有効にするのには false (0) にします。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |省略可能  <br/> |図形に図形データ項目へのユーザーの変更を上書きするかどうかにより、データ レコード セットが更新されたとき、データにリンクされています。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |図形をコピーまたはカットするときに図形データのリンクを処理する方法を定義します。 接続先の図形内の既存のリンクを置換するのには 1 です。 接続先の図形内の既存のリンクを維持するために 0 を返します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |省略可能  <br/> |主キーとしてデータ レコード セット内の行の順序を使用するかどうか。 行 Id は、行の順序によって決定する場合は true (1)。 False (0) 場合は、行 Id は、データ レコード セットの主キー列の値によって決定されます。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |省略可能  <br/> |日付と時刻のデータ レコード セットが最後に更新します。  <br/> |Xsd:dateTime の値を入力します。  <br/> |
   

