---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2ed8bace97dee3842243ed835769e80e8aaf6b03
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387532"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーの形式に影響するイベント通知を登録します。
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>パラメーター

 _pAdvise_
  
> [in]ビューへのポインターでは、後続の通知を受信するシンク オブジェクトを案内します。 
    
 _pulConnection_
  
> [out]成功した通知の登録を表す、0 以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が正常に完了しました。
    
E_OUTOFMEMORY 
  
> 登録にメモリ不足のため失敗しました。
    
## <a name="remarks"></a>備考

フォーム ビューアーでは、フォームに変更が発生したときに通知を登録するのには、フォームの**IMAPIForm::Advise**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

ビューのコピーを保存では、適切な[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドを呼び出すイベントが発生したときにそれを使用できるように、 _pAdvise_パラメーターで渡されたシンク ポインターを案内します。 呼び出しビューは、通知の登録をキャンセルするまで、ポインターを保持するシンクの[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx)の方法を案内します。 _PulConnection_パラメーターの内容を 0 以外の値に設定します。 
  
多くのフォームは、登録とイベントの後続の通知を処理するヘルパー オブジェクトを実装します。 
  
通知プロセスの詳細については一般に、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
通知およびフォームの詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MAPI のイベント通知](event-notification-in-mapi.md)
  
[フォーム通知の送受信](sending-and-receiving-form-notifications.md)

