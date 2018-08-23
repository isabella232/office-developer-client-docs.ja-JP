---
title: PidTagPstConfigurationFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b79b40a59a2bf7b68c58bffbccca04034b853a15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570206"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>PidTagPstConfigurationFlags 標準プロパティ
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
個人用領域 (.pst ファイル) テーブルの構成フラグをオン表示されるようです。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|識別子:  <br/> |0x6770  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |パーソナル ストレージ表 (.pst) 内部  <br/> |
   
## <a name="remarks"></a>注釈

以下は、このプロパティの有効な値です。
  
PST_CONFIG_UNICODE
  
> Unicode の .pst ファイルを示します。 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> クライアントから設定フラグ、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドを**ConfigureMsgService**を[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)の呼び出しと同様に扱われ、「このインフォメーション サービスが構成されていません」をスキップ警告します。 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を変更するのには**ConfigureMsgService**は、指定されていてもに指示します。 その場合は、新しい .pst ファイルに対してのみ、指定されました。
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> 構成コードは、オフライン フォルダー (.ost) ファイルがされているかどうかを確認するダイアログ ボックスが、ユーザーの応答によって検出されたオフライン フォルダーを使用してか、または別のオフライン フォルダーを参照するユーザーを有効にする最初に表示するように指示します。
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> 新しい一意の名前を使用して .ost ファイルをコピーし、現在の名前を破棄します。 既存の .ost ファイルは、コンピューター上に残りますが、このプロファイルでは使用されなく。 これは通常、Microsoft Outlook は、特定の .ost ファイルを許可しないと、レジストリ ポリシーは、ファイルの名前を変更するユーザーを許可しない場合に発生します。 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

