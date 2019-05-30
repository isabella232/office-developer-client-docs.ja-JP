---
title: DataRecordSet 要素 (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539678"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordSet 要素 (DataRecordSets_Type complexType) (Visio XML)

Microsoft Visio のデータベースからクエリされたデータを格納、書式設定、更新、および公開します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |recordsets  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |文書内のすべての**DataRecordset**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Ado の従来の XML スキーマに準拠し、データレコードセットのデータを記述する XML が保存されています。  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |ユーザーインターフェイスで実行された前回正常に完了した自動リンクアクションの図形データ項目と親**DataRecordset**要素の列を比較するルールを定義します。  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Visio ユーザーインターフェイスの [**外部データ**] ウィンドウにデータ列を表示する方法を定義し、データの種類と書式を定義することによって、列のデータを修飾します。  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データレコードセット内のすべての**DataColumn**要素を含みます。  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |データレコードセット内の1つまたは複数の主キー列を指定します。  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |データレコードセットの更新後に競合している図形にリンクされているデータレコードセット内の行を示します。  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |データレコードセットの行を図形にマップします。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|チェックサム  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |Visio によって生成される、データレコードセットのプロパティに基づいたチェックサム値。 この attirbute を0に設定します。Visio は、この値を実行時に再計算します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|Command  <br/> |xsd: string  <br/> |省略可能  <br/> |データソースからのデータのクエリに使用されるコマンド文字列。  <br/> |Xsd: string 型の値。  <br/> |
|ConnectionID  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |関連付けられている**DataConnection**オブジェクトの接続 ID。 XML データソースには存在しません。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|ID  <br/> |xsd: アン Signedint  <br/> |必須  <br/> |データレコードセットの ID。ドキュメント内で一意です。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |データレコードセットの表示名 (フレンドリ名) を指定します。  <br/> |Xsd: string 型の値。  <br/> |
|NextRowID  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |次に使用可能な Visio の行 ID。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|選択肢  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |データレコードセットに適用するオプション。 指定できる値は、次の表に示す1つ以上の値の組み合わせです。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|RefreshInterval  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |Visio がデータレコードセットを自動的に更新する頻度 (分単位)。 この値は、1以上である必要があります。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd: boolean  <br/> |省略可能  <br/> |データ調整のユーザーインターフェイスを無効にする必要があるかどうか。 ユーザーインターフェイス (UI) を無効にする場合は True (1)。 False (0) UI を有効にします。  <br/> |Xsd: boolean 型の値。  <br/> |
|RefreshOverwriteAll  <br/> |xsd: boolean  <br/> |省略可能  <br/> |データレコードセットが更新されたときに、データにリンクされている図形の図形データ項目に対するユーザーの変更を上書きするかどうかを指定します。  <br/> |Xsd: boolean 型の値。  <br/> |
|ReplaceLinks  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |図形をコピーまたは切り取るときの、図形データのリンクの処理方法を定義します。 ターゲット図形の既存のリンクを置き換える場合は、1を入力します。 ターゲット図形の既存のリンクを維持する場合は0。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|RowOrder  <br/> |xsd: boolean  <br/> |省略可能  <br/> |データレコードセット内の行の順序を主キーとして使用するかどうかを指定します。 行 Id が行の順序によって決まる場合は、True (1) を指定します。 False (0) 行 Id がデータレコードセットの主キー列 (複数可) の値で決定されている場合です。  <br/> |Xsd: boolean 型の値。  <br/> |
|TimeRefreshed  <br/> |xsd: dateTime  <br/> |省略可能  <br/> |データレコードセットが最後に更新された日付と時刻。  <br/> |Xsd: dateTime 型の値。  <br/> |
   

