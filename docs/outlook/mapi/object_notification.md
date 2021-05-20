---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430169"
---
# <a name="object_notification"></a>OBJECT_NOTIFICATION

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コピーや変更など、変更を受けたオブジェクトに関する情報を格納します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a>Members

 **cbEntryID**
  
> **lpEntryID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpEntryID**
  
> 影響を受けるオブジェクトのエントリ識別子へのポインター。
    
 **ulObjType**
  
> 影響を受けるオブジェクトの種類。 使用できる型は次のとおりです。
    
MAPI_STORE 
  
> メッセージ ストア。 
    
MAPI_ADDRBOOK 
  
> アドレス帳。 
    
MAPI_FOLDER 
  
> フォルダー。
    
MAPI_ABCONT 
  
> アドレス帳コンテナー。
    
MAPI_MESSAGE 
  
> メッセージ。
    
MAPI_MAILUSER 
  
> メッセージング ユーザー。
    
MAPI_ATTACH 
  
> 添付ファイル。
    
MAPI_DISTLIST 
  
> 配布リスト。
    
MAPI_PROFSECT 
  
> [プロファイル] セクション。
    
MAPI_STATUS 
  
> Status オブジェクト。
    
MAPI_SESSION 
  
> Session オブジェクト。
    
 **cbParentID**
  
> **lpParentID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpParentID**
  
> 影響を受けるオブジェクトの親のエントリ識別子へのポインター。
    
 **cbOldID**
  
> **lpOldID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpOldID**
  
> 元のオブジェクトのエントリ識別子へのポインター。 イベントで元のオブジェクトが必要ない場合は、このポインターを NULL にできます。
    
 **cbOldParentID**
  
> **lpOldParentID** メンバーが指すエントリ識別子のバイト数。 
    
 **lpOldParentID**
  
> 元のオブジェクトの親のエントリ識別子へのポインター。 イベントで元のオブジェクトが必要ない場合は、このポインターを NULL にできます。
    
 **lpPropTagArray**
  
> イベントの影響 [を受けるプロパティを](sproptagarray.md) 識別するプロパティ タグを含む SPropTagArray 構造体へのポインター。 
    
## <a name="remarks"></a>注釈

この **OBJECT_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。 **NOTIFICATION** **構造体の info** メンバーに OBJECT_NOTIFICATION構造体が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは、次のいずれかの種類のイベントに設定されます。 
  
- fnevObjectCreated
    
- fnevObjectModified
    
- fnevObjectDeleted
    
- fnevObjectMoved
    
- fnevObjectCopied
    
- fnevSearchComplete
    
fnevSearchComplete イベントの種類で表される検索完了イベントは、1 つの検索フォルダーのドメインの最初の検索が完了したかどうかを示します。
  
元のオブジェクトに関する情報を含む次のメンバーは、移動イベントとコピー イベントでのみ使用されます。 
  
- **cbOldID**
    
- **lpOldID**
    
- **cbOldParentID**
    
- **lpOldParentID**
    
これらのメンバーは、他の種類のイベントには適用されません。
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
## <a name="see-also"></a>関連項目



[�ʒm](notification.md)
  
[SPropTagArray](sproptagarray.md)


[MAPI の構造](mapi-structures.md)

