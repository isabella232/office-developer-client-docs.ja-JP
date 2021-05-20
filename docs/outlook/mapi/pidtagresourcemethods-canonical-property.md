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
  
status オブジェクトでサポートされている **IMAPIStatus** インターフェイスのメソッドを示すフラグのビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_RESOURCE_METHODS  <br/> |
|識別子:  <br/> |0x3E02  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、ステータス オブジェクトの **IMAPIStatus** の実装でサポートされているメソッドを示します。 Status オブジェクトは、サポートされていないメソッドMAPI_E_NO_SUPPORTを返します。 
  
クライアントは、サポートされていないメソッドを **呼びPR_RESOURCE_METHODS** を避けるために、status オブジェクトのプロパティを使用します。 特定のメソッドに対応するフラグが設定されている場合は、メソッドが存在し、呼び出し可能です。 このフラグがクリアされている場合は、メソッドを呼び出す必要があります。 
  
MAPI によって実装された状態オブジェクトは、次のメソッドをサポートしています。
  
|**Status オブジェクト**|**サポートされているメソッド**|
|:-----|:-----|
|MAPI サブシステム  <br/> |**ValidateState** のみ  <br/> |
|MAPI アドレス帳  <br/> |**ValidateState** のみ  <br/> |
|MAPI スプーラー  <br/> |**ValidateState** と **FlushQueues** <br/> |
   
次のフラグの 1 つ以上は、次の **PR_RESOURCE_METHODS。**
  
STATUS_CHANGE_PASSWORD 
  
> [IMAPIStatus::ChangePassword](imapistatus-changepassword.md)メソッドがサポートされています。 
    
STATUS_FLUSH_QUEUES 
  
> [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドがサポートされています。 
    
STATUS_SETTINGS_DIALOG 
  
> [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)メソッドがサポートされています。 
    
STATUS_VALIDATE_STATE 
  
> [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドがサポートされています。 
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

