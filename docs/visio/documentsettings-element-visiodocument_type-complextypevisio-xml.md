---
title: DocumentSettings 要素 (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: ドキュメント設定を指定する要素が含まれます。
ms.openlocfilehash: 6c7f8e4c8009229664d643d4fcc7408bf3987f38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590297"
---
# <a name="documentsettings-element-visiodocument_type-complextype-visio-xml"></a>DocumentSettings 要素 (VisioDocument_Type complexType) (Visio XML)

ドキュメント設定を指定する要素が含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft ドキュメントのルートVisioです。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |カスタム ツールバーを表す MIME (Multipurpose Internet Mail Extensions) でエンコードされた Microsoft Visio (VSU) ファイル。  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |ドキュメントのカスタム メニューとアクセラレータVisio定義する Microsoft ユーザー インターフェイス (.vsu) ファイルの名前が含まれる。  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |ドキュメントのカスタム ツールバーとステータス バー Visio定義する Microsoft Visio ユーザー インターフェイス (.vsu) ファイルの名前を含んでいます。  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |ドキュメントまたはウィンドウのダイナミック グリッド機能を有効にするかどうかを指定します。  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |図面で接着が有効な場合に、図形が接着するオブジェクトを指定します。  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |ユーザーがバックグラウンド ページを削除または編集できるかどうかを指定します。  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |ユーザーがマスターマスターの作成、編集、または削除を防止するかどうかを指定します。 この設定に関係なく、ユーザーは引き続きマスター のインスタンスを作成できます。  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |ユーザーが **LockSelect** 要素が 1 に設定されている図形を選択しないかどうかを指定します。  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |ユーザーがスタイルの作成または編集を妨げるかどうかを指定します。  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |**SnapAngle** 要素のコレクションが含まれます。  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |アクティブなウィンドウに対して、特定スナップの拡張情報の設定を有効または無効にするかどうかを指定します。  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |ウィンドウでスナップがアクティブな場合に、図形のスナップ先のオブジェクトを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |StyleSheet 要素の ID **を指定** します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |StyleSheet 要素の ID **を指定** します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |StyleSheet 要素の ID **を指定** します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |StyleSheet 要素の ID **を指定** します。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|TopPage  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |Microsoft ユーザーがドキュメントを開く際に表示するページの ID をVisio。  <br/> |xsd:unsignedInt 型の値。  <br/> |
   

