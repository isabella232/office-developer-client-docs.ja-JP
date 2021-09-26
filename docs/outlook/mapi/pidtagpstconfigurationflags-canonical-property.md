---
title: PidTagPstConfigurationFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eccf22a9e2fc39f4232eb194bef204055ec3ba07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583241"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>PidTagPstConfigurationFlags 標準プロパティ
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用ストレージ テーブル (.pst ファイル) の構成フラグを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|識別子:  <br/> |0x6770  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |個人用ストレージ テーブル (.pst) 内部  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの有効な値を次に示します。
  
PST_CONFIG_UNICODE
  
> Unicode .pst ファイルを示します。 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> クライアント フラグから [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) メソッドに設定すると **、ConfigureMsgService** は [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) 呼び出しのように扱い、「この情報サービスが構成されていません」という警告をスキップします。 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> **ConfigureMsgService に**、指定された場合でも、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を変更しなくします。 その場合は、新しい .pst ファイルにのみ提供されました。
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> 構成コードに、最初にダイアログ ボックスを表示して、オフライン フォルダー (.ost) ファイルが見つかったかどうかを確認し、ユーザーの応答に応じて、見つかったオフライン フォルダーを使用するか、ユーザーが別のオフライン フォルダーを参照できるようになります。
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> 新しい一意の名前を持つ .ost ファイルをコピーし、現在の名前を破棄します。 既存の .ost ファイルはコンピューター上に残りますが、このプロファイルでは使用されなくなりました。 これは通常、Microsoft Outlook特定の .ost ファイルが許可されなくなった場合に発生し、レジストリ ポリシーによってユーザーがファイルの名前を変更できない場合に発生します。 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]] 
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

