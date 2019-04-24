---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346838"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
スレッドの安全性を確保するために既存のアドバイズシンクをラップするアドバイズシンクを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番ラップするアドバイズシンクへのポインター。 
    
 _lppAdviseSink_
  
> 読み上げ_lpAdviseSink_パラメーターで指定されたアドバイズシンクをラップする新しいアドバイズシンクへのポインターへのポインター。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>解説

ラッパーの目的は、 **HrThisThreadAdviseSink**関数を呼び出したのと同じスレッドで通知が呼び出されるようにすることです。 この関数は、特定のスレッドで実行する必要がある通知コールバックを保護するために使用されます。 
  
クライアントアプリケーションは、 **HrThisThreadAdviseSink**を使用して通知を生成するタイミングを制限する必要があります。つまり、前のアドバイスでクライアントによって渡されたアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドに対して呼び出しが行われたときです。 **** 呼び出し。 通知を任意に生成することが許可されている場合、通知の実装によって、クライアントが適切でない場合には、マルチスレッド操作になることがあります。 たとえば、クライアントは、Microsoft Foundation クラスライブラリの1つなど、マルチスレッド呼び出しをサポートしていないライブラリを使用する場合があります。 別のスレッドで通知を行うと、このようなクライアントはテストが難しくなり、エラーが発生しやすくなります。 
  
 **HrThisThreadAdviseSink**は、次の適切な時間にのみ、 **onnotify**呼び出しが発生することを確認します。 
  
- MAPI メソッドの呼び出しの処理中。 
    
- Windows メッセージの処理中。 
    
**HrThisThreadAdviseSink**が実装されている場合、すべてのスレッドで新しいアドバイズシンクの**onnotify**メソッドを呼び出すと、 **HrThisThreadAdviseSink**が呼び出されたスレッドで元の通知方法が実行されます。 
  
通知およびアドバイズシンクの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」および「[アドバイズシンクオブジェクトの実装](implementing-an-advise-sink-object.md)」を参照してください。 
  

