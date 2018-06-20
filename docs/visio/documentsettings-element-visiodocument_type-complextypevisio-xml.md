---
title: DocumentSettings 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: ドキュメントの設定を指定する要素が含まれています。
ms.openlocfilehash: 8cd10e43b95918ccd2ceaa75a47c9e93de2acc14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805256"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSettings 要素 (VisioDocument_Type complexType)'Visio XML (')

ドキュメントの設定を指定する要素が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft Visio ドキュメントのルート要素です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |MIME (多目的インターネット メール拡張機能) では、Microsoft Visio ユーザー インターフェイス (VSU) ファイルをユーザー設定のツールバーを表すエンコードされています。  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |カスタム メニューおよびアクセラレータのドキュメントを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |ユーザー設定ツールバーおよびドキュメントのステータス バーを定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前が含まれています。  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウのダイナミック グリッド機能が有効になっているかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |ドキュメントで接着が有効になっているときに図形が接着するオブジェクトを指定します。  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |削除したり、背景ページを編集ユーザーを禁止するかどうかを指定します。  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |作成、編集、またはマスター シェイプを削除してからユーザーを防止するかどうかを指定します。 この設定に関係なく、ユーザーのマスター シェイプのインスタンスを作成できます。  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |ユーザーがその**lockselect] を有効**要素を 1 に設定されている図形を選択できないとしているかどうかを指定します。  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |かどうかユーザーできません作成または編集するスタイルを指定します。  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**SnapAngle**要素のコレクションが含まれています。  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |特定のスナップインの拡張機能の設定が有効か、作業中のウィンドウを無効になっているかどうかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |図形のスナップとスナップがアクティブなウィンドウ内でオブジェクトを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |**スタイル シート**の要素の ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |**スタイル シート**の要素の ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |**スタイル シート**の要素の ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |**スタイル シート**の要素の ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|TopPage  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |Microsoft Visio でドキュメントを開いたときに表示されるページの ID を指定します。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
   

