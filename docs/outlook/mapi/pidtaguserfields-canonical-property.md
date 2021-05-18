---
title: PidTagUserFields 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360740"
---
# <a name="pidtaguserfields-canonical-property"></a>PidTagUserFields 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー定義フィールドに関する名前、データ型、その他の情報が含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_USERFIELDS  <br/> |
|識別子:  <br/> |0x36E3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>注釈

各アイテムについて、Outlookは、対応する **IMessage** オブジェクトの [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティ内のすべてのユーザー定義フィールドの定義を格納します。 **PidLidPropertyDefinitionStream** プロパティには、フィールド定義を含む [PropertyDefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリ ストリームが含まれます。 フィールド定義のストリーム構造の詳細については [、「Stream Structures」を参照してください](stream-structures.md)。
  
フォルダーごとに、Outlook は、そのフォルダー内のすべてのユーザー定義フィールドの定義を、メッセージ クラス IPC.MS の関連付けられたメッセージの **PidTagUserFields** プロパティに格納します。REN。USERFIELDS - 関連付けられたコンテンツ テーブルにこのクラスのメッセージが 1 つ以上含まれていると推定される各フォルダー。 
  
> [!NOTE]
> フォルダー内のユーザー定義フィールドのセットは、必ずしも各アイテムのユーザー定義フィールドのセットと一致しない場合があります。 
  
フォルダー内のユーザー定義フィールドのセットは、フォルダーの Field Chooser など、Outlook UI のさまざまな場所に表示されます。 メッセージの **PidTagUserFields** プロパティには、フォルダー フィールド定義を含むバイナリ ストリーム **FolderUserFields** が含まれます。 フォルダー フィールド定義のストリーム構造の詳細については [、「Folder Fields Stream Structures」](folder-fields-stream-structures.md) および [「FolderUserFields Stream Sample」を参照してください](folderuserfields-stream-sample.md)。
  
## <a name="section-heading"></a>セクション見出し

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

