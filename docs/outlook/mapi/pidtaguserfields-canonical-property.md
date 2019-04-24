---
title: PidTagUserFields 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360740"
---
# <a name="pidtaguserfields-canonical-property"></a>PidTagUserFields 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー定義フィールドの名前、データ型、およびその他の情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_USERFIELDS  <br/> |
|識別子:  <br/> |0x36E3  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>解説

各アイテムについて、Outlook は、すべてのユーザー定義フィールドの定義を対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティに格納します。 **PidLidPropertyDefinitionStream**プロパティには、フィールド定義を含む[propertydefinition](propertydefinition-stream-structure.md)と呼ばれるバイナリストリームが含まれています。 フィールド定義のストリーム構造の詳細については、「 [stream 造](stream-structures.md)」を参照してください。
  
各フォルダーについて、Outlook は、メッセージクラス IPC.MS の関連付けられたメッセージの**PidTagUserFields**プロパティに、そのフォルダー内のすべてのユーザー定義フィールドの定義を格納します。REN.userfields-各フォルダーは、関連付けられた contents テーブルにこのクラスのメッセージを1つだけ含めることを想定していました。 
  
> [!NOTE]
> フォルダー内のユーザー定義フィールドのセットは、各アイテムのユーザー定義フィールドのセットと必ずしも一致しない場合があります。 
  
フォルダー内のユーザー定義フィールドのセットは、フォルダーの [フィールドの選択] など、Outlook UI 内のさまざまな場所に表示されます。 メッセージの**PidTagUserFields**プロパティには、フォルダーフィールドの定義を含むバイナリストリーム、 **folderuserfields**が含まれています。 フォルダーフィールド定義のストリーム構造の詳細については、「 [folder Fields stream 構造](folder-fields-stream-structures.md)」および「 [folderuserfields stream Sample](folderuserfields-stream-sample.md)」を参照してください。
  
## <a name="section-heading"></a>セクション見出し

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[Outlook のアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[propertydefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

