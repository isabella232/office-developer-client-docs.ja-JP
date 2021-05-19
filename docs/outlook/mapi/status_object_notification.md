---
title: STATUS_OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STATUS_OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: 2872130d-a36b-46ea-bfd1-4700fe3dd41b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 84b44b4b054a2b2617502a6a463a6d4a89546804
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426269"
---
# <a name="status_object_notification"></a>STATUS_OBJECT_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
変更の影響を受けた状態オブジェクトについて説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG cValues;
  LPSPropValue lpPropVals;
} STATUS_OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> **lpEntryID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpEntryID**
  
> 変更された状態オブジェクトのエントリ識別子へのポインター。
    
 **cValues**
  
> [lpPropVals](spropvalue.md)メンバーが指す配列内の **SPropValue 構造体の** 数。 
    
 **lpPropVals**
  
> 変更された状態オブジェクトの **プロパティを記述する SPropValue** 構造体の配列へのポインター。 
    
## <a name="remarks"></a>注釈

このSTATUS_OBJECT_NOTIFICATIONは、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md)つです。  この **STATUS_OBJECT_NOTIFICATION** は  _、fnevStatusObjectModified_ 型のイベントの状態オブジェクト通知に含まれています。 Status オブジェクト通知は、内部 MAPI 通知です。クライアントとサービス プロバイダーは、クライアントとサービス プロバイダーに登録できません。また、サービス プロバイダーはクライアントを生成できません。
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが **IMAPISupport** メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropValue](spropvalue.md)


[MAPI の構造](mapi-structures.md)

