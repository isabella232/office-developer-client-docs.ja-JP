---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f9375bea70521ead0659f51413301be170559ac5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616958"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
スレッドの安全性を確保するために既存のアアドバイス シンクをラップするアアドバイス シンクを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>パラメーター

 _lpAdviseSink_
  
> [in]ラップするアアドバイス シンクへのポインター。 
    
 _lppAdviseSink_
  
> [out]  _lpAdviseSink_ パラメーターが指すアアドバイス シンクをラップする新しいアアドバイス シンクへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>注釈

ラッパーの目的は **、HrThisThreadAdviseSink** 関数と呼ばれる同じスレッドで通知が呼び出されるのを確認します。 この関数は、特定のスレッドで実行する必要がある通知コールバックを保護するために使用されます。 
  
クライアント アプリケーションは **、HrThisThreadAdviseSink** を使用して、以前の Advise 呼び出しでクライアントによって渡されたアアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドへの呼び出しが行われたときに、通知が生成される時間を制限する必要があります。 通知を任意に生成できる場合、通知の実装によって、クライアントが適切ではない場合にマルチスレッド操作を強制する場合があります。 たとえば、クライアントは、マルチスレッド呼び出しをサポートしない Microsoft Foundation クラス ライブラリの 1 つなどのライブラリを使用する場合があります。 別のスレッドに通知すると、このようなクライアントのテストが困難になり、エラーが発生しやすくなります。 
  
 **HrThisThreadAdviseSink** は **、OnNotify** 呼び出しが次の適切な時間にのみ発生することを確認します。 
  
- MAPI メソッドの呼び出しの処理中。 
    
- メッセージの処理Windows。 
    
**HrThisThreadAdviseSink** が実装されると、任意のスレッドで新しいアアドバイス シンクの **OnNotify** メソッドを呼び出した場合 **、HrThisThreadAdviseSink** が呼び出されたスレッドで元の通知メソッドが実行されます。 
  
通知と通知シンクの詳細については [、「MAPI](event-notification-in-mapi.md) でのイベント通知」および「アアドバイス シンク オブジェクトの実装」 [を参照してください](implementing-an-advise-sink-object.md)。 
  

