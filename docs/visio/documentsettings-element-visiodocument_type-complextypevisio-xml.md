---
title: DocumentSettings 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: ドキュメントの設定を指定する要素を格納します。
ms.openlocfilehash: 0d8e0809afae7b3de059166343577bb58f0eb01b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540071"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSettings 要素 (VisioDocument_Type complexType) (Visio XML)

ドキュメントの設定を指定する要素を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書の xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft Visio 図面のルート要素です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |カスタムツールバーを表す MIME (多目的インターネットメール内線) でエンコードされた Microsoft Visio ユーザーインターフェイス (VSU) ファイル。  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |文書のカスタムメニューとアクセラレータを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |文書のカスタムツールバーおよびステータスバーを定義する Microsoft Visio ユーザーインターフェイス (vsu) ファイルの名前が含まれています。  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウに対して動的グリッド機能を有効にするかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |図面で接着が有効になっている場合に、図形を接着するオブジェクトを指定します。  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |ユーザーが背景ページを削除または編集できないようにするかどうかを指定します。  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |ユーザーがマスターシェイプの作成、編集、または削除をできないようにするかどうかを指定します。 この設定にかかわらず、ユーザーは引き続きマスターシェイプのインスタンスを作成できます。  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |ユーザーが**Lockselect**要素が1に設定されている図形を選択できないようにするかどうかを指定します。  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |ユーザーがスタイルを作成または編集できないようにするかどうかを指定します。  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**Snapangle**要素のコレクションを格納します。  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |アクティブウィンドウに対して特定のスナップ延長の設定を有効にするか無効にするかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |ウィンドウのスナップがアクティブなときに、図形をスナップするオブジェクトを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |**StyleSheet**要素の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|DefaultGuideStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |**StyleSheet**要素の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|DefaultLineStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |**StyleSheet**要素の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|DefaultTextStyle  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |**StyleSheet**要素の ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|TopPage  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |Microsoft Visio で文書を開くときに表示されるページの ID を指定します。  <br/> |Xsd:/Signedint 型の値。  <br/> |
   

