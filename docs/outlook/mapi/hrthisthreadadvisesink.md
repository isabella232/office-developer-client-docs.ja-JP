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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800344"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**適用されます**: Outlook 
  
スレッドの安全のための既存のアドバイズ シンクをラップするアドバイズ シンクを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpAdviseSink_
  
> [in]ラップするアドバイズ シンクへのポインター。 
    
 _lppAdviseSink_
  
> [out]_LpAdviseSink_パラメーターが指す、アドバイズ シンクをラップする新しいアドバイズ シンクへのポインターへのポインターです。 
    
## <a name="return-value"></a>Return value

なし。
  
## <a name="remarks"></a>備考

ラッパーでは、通知が**HrThisThreadAdviseSink**関数を呼び出した同じスレッドで呼び出されることになっていることを確認します。 この関数は、特定のスレッド上で実行する必要があります通知コールバックを保護するために使用されます。 
  
クライアント アプリケーションは、通知が生成されるときは、クライアントが以前の**のアドバイスで渡されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドがコールされたときに制限するのには**HrThisThreadAdviseSink**を使用する必要があります。** を呼び出します。 任意に生成するのには、通知が許可されている場合通知の実装可能性があります、クライアントにマルチ スレッド処理がこれに該当する場合。 たとえば、クライアントは、マルチ スレッドの呼び出しをサポートしていない Microsoft Foundation クラス ライブラリのいずれかのライブラリを使用する場合があります。 別のスレッドに通知は、このようなクライアント、テストが困難で、エラーを起こしやすい。 
  
 **HrThisThreadAdviseSink**は、 **OnNotify**呼び出しは、これらの適切な時刻にのみ発生することを確認します。 
  
- 中の任意の MAPI メソッドの呼び出しを処理します。 
    
- Windows メッセージの処理します。 
    
**HrThisThreadAdviseSink**が実装されると、任意のスレッドでの新規のアドバイズ シンクの**OnNotify**メソッドへの呼び出しは、 **HrThisThreadAdviseSink**が呼び出された対象のスレッドで実行される元の通知方法を発生します。 
  
通知の詳細については、アドバイズ シンク[で MAPI イベント通知](event-notification-in-mapi.md)と[通知シンク オブジェクトを実装する](implementing-an-advise-sink-object.md)を参照してください。 
  

