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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408944"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>PidTagPstConfigurationFlags 標準プロパティ
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
タイプの個人用ストレージテーブル (.pst ファイル) の構成フラグ。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|識別子:  <br/> |0x6770  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |パーソナルストレージテーブル (.pst) 内部  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの有効な値は次のとおりです。
  
PST_CONFIG_UNICODE
  
> Unicode .pst ファイルを示します。 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> クライアントフラグから[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに設定した場合は、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)呼び出しのような**ConfigureMsgService**を処理し、"この information service は構成されていません" を省略します。メッセージ. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値が指定されていても、その値を変更しないように**ConfigureMsgService**に指示します。 その場合は、新しい .pst ファイルに対してのみ提供されています。
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> 最初に、オフラインフォルダー (.ost) ファイルが見つかったかどうかを確認するダイアログボックスを表示し、ユーザーの応答に応じて、見つかったオフラインフォルダーを使用するか、ユーザーが別のオフラインフォルダーを参照できるようにするように指示します。
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> .ost ファイルを新しい一意の名前でコピーし、現在の名前を破棄します。 既存の .ost ファイルはコンピューターに残りますが、このプロファイルでは使用されなくなります。 これは通常、Microsoft Outlook で特定の .ost ファイルが許可されなくなり、レジストリポリシーによってユーザーがファイルの名前を変更できない場合に発生します。 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]] 
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

