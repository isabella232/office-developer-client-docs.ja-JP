---
title: DataRecordSet 要素 (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Microsoft Visio のデータベースからクエリしたデータを保存、書式設定、更新、および公開します。
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539678"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>DataRecordSet 要素 (DataRecordSets_Type complexType) (Visio XML)

Microsoft Visio のデータベースからクエリしたデータを保存、書式設定、更新、および公開します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**名詞空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |ドキュメント内のすべての **DataRecordset** 要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |ADO レコードセット用の ADO クラシック XML スキーマに準拠する XML を格納します。データ レコードセット内のデータは、この XML で記述します。  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |ユーザー インターフェイスで最後に正常に実行された自動リンク アクションからの図形データ アイテムと、親 **DataRecordset** 要素内の列を比較するルールを定義します。  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Visio ユーザー インターフェイスの **[外部データ]** ウィンドウにデータ列を表示する方法を定義し、データ型と書式を定義することで列内のデータを修飾します。  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |データ レコードセット内のすべての **DataColumn** 要素を格納します。  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |データ レコードセット内で 1 つ以上の主キー列を識別します。  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |図形にリンクされたデータ レコードセット内の行で、データ レコードセットの更新後に競合した状態になっているものを示します。  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |データ レコードセットの行を図形にマップします。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|Checksum  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |Visio によって生成されたチェックサム値。データ レコードセットのプロパティに基づいています。 この属性を 0 に設定すると、この値が実行時に Visio によって再計算されます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Command  <br/> |xsd:string  <br/> |省略可能  <br/> |データ ソースからデータをクエリする際に使用されるコマンド文字列。  <br/> |xsd:string 型の値。  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |関連する **DataConnection** オブジェクトの接続 ID。 XML データ ソースの場合は存在しません。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |データ レコードセットの ID。ドキュメント内で一意になります。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |データ レコードセットの表示名 (フレンドリ名)。  <br/> |xsd:string 型の値。  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |次に利用可能な Visio 行の ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|Options  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |データ レコードセットに適用するオプション。 次の表に示した 1 つ以上の任意の組み合わせの値を使用できます。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |Visio が自動的にデータ レコードセットを更新する間隔 (分単位)。 この値は 1 以上にする必要があります。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |省略可能  <br/> |データ調整ユーザー インターフェイスを無効にする必要があるかどうか。 True (1) にすると、このユーザー インターフェイス (UI) が無効になります。 False (0) にすると、この UI が有効になります。  <br/> |xsd:boolean 型の値。  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |省略可能  <br/> |データ レコードセットが更新されたときに、データにリンクされた図形内の図形データ アイテムに対するユーザーの変更を上書きするかどうか。  <br/> |xsd:boolean 型の値。  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |図形がコピーまたは切り取られたときに、どのように図形データのリンクを処理するかを定義します。 ターゲットの図形で既存のリンクを置き換える場合は 1。 ターゲットの図形で既存のリンクを維持する場合は 0。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |省略可能  <br/> |データ レコードセットでの行の順序を主キーとして使用するかどうか。 行の順序で行 ID を決定する場合は True (1)。 データ レコードセットの主キー列の値で行 ID を決定する場合は False (0)。  <br/> |xsd:boolean 型の値。  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |省略可能  <br/> |データ レコードセットが最後に更新された日付と時刻。  <br/> |xsd:dateTime type 型の値。  <br/> |
   

