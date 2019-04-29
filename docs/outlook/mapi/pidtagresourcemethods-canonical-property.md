---
title: PidTagResourceMethods 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e9aee3280edbed60e97ef6e00e61f3086f6f07ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436336"
---
# <a name="pidtagresourcemethods-canonical-property"></a>PidTagResourceMethods 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態オブジェクトでサポートされている**imapistatus**インターフェイスのメソッドを示すフラグのビットマスクを含みます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_METHODS  <br/> |
|識別子:  <br/> |0x3e02  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、ステータスオブジェクトの**imapistatus**の実装のどのメソッドがサポートされているかを示します。 Status オブジェクトは、サポートされていないメソッドから MAPI_E_NO_SUPPORT を返すことができます。 
  
クライアントは、ステータスオブジェクトの**PR_RESOURCE_METHODS**プロパティを使用して、サポートされていないメソッドを呼び出すことを回避します。 特定のメソッドに対応するフラグが設定されている場合、メソッドが存在し、呼び出すことができます。 このフラグがオフの場合は、メソッドを呼び出すことはできません。 
  
MAPI によって実装される状態オブジェクトは、次の方法をサポートします。
  
|**Status オブジェクト**|**サポートされているメソッド**|
|:-----|:-----|
|MAPI サブシステム  <br/> |**validatestate**のみ  <br/> |
|MAPI アドレス帳  <br/> |**validatestate**のみ  <br/> |
|MAPI スプーラー  <br/> |**validatestate**および**flushqueues** <br/> |
   
**PR_RESOURCE_METHODS**では、次のフラグのうち1つ以上を設定できます。
  
STATUS_CHANGE_PASSWORD 
  
> [imapistatus:: ChangePassword](imapistatus-changepassword.md)メソッドがサポートされていることを示します。 
    
STATUS_FLUSH_QUEUES 
  
> [imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドがサポートされていることを示します。 
    
STATUS_SETTINGS_DIALOG 
  
> [imapistatus:: settingsdialog](imapistatus-settingsdialog.md)メソッドがサポートされていることを示します。 
    
STATUS_VALIDATE_STATE 
  
> [imapistatus:: validatestate](imapistatus-validatestate.md)メソッドがサポートされていることを示します。 
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

