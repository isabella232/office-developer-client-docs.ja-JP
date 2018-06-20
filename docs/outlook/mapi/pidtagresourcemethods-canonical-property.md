---
title: PidTagResourceMethods の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceMethods
api_type:
- COM
ms.assetid: 60ebbcd5-b758-4c96-b8ec-089e0aae1a5f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f346baf303db9da765eec183d168b370547ec2de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803342"
---
# <a name="pidtagresourcemethods-canonical-property"></a>PidTagResourceMethods の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
**IMAPIStatus**インタ フェース内の状態のオブジェクトでサポートされているメソッドを示すフラグのビットマスクを格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_RESOURCE_METHODS  <br/> |
|識別子:  <br/> |0x3E02  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、サポート対象の**IMAPIStatus**の実装では、状態オブジェクトのメソッドを示します。 状態オブジェクトは、サポートされていないメソッドから MAPI_E_NO_SUPPORT を返すことができます。 
  
クライアントは、サポートされていないメソッドの呼び出しを避けるために、状態オブジェクトの**PR_RESOURCE_METHODS**プロパティを使用します。 特定のメソッドに対応するフラグが設定されている場合、メソッドが存在し、呼び出すことができます。 このフラグがオフの場合は、このメソッドは呼び出さないでください。 
  
状態オブジェクトは、MAPI のサポートで次のメソッドを実装しました。
  
|**ステータス オブジェクト**|**サポートされている方法**|
|:-----|:-----|
|MAPI サブシステム  <br/> |**ValidateState**のみ  <br/> |
|MAPI アドレス帳  <br/> |**ValidateState**のみ  <br/> |
|MAPI スプーラー  <br/> |**ValidateState**と**FlushQueues** <br/> |
   
**PR_RESOURCE_METHODS**では、次のフラグの 1 つ以上を設定できます。
  
STATUS_CHANGE_PASSWORD 
  
> [IMAPIStatus::ChangePassword](imapistatus-changepassword.md)メソッドがサポートされていることを示します。 
    
STATUS_FLUSH_QUEUES 
  
> [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドがサポートされていることを示します。 
    
STATUS_SETTINGS_DIALOG 
  
> [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドがサポートされていることを示します。 
    
STATUS_VALIDATE_STATE 
  
> [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートされていることを示します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

