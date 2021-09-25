---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 398644605e3ad1020ce594bc8d74593fdede6ad4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567600"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームに影響を与えるイベントに関する通知用にフォーム ビューアーを登録します。
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>パラメーター

 _pAdvise_
  
> [in]ビューへのポインターは、後続の通知を受け取るシンク オブジェクトに通知します。 
    
 _pulConnection_
  
> [out]正常な通知登録を表す 0 以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録が成功しました。
    
E_OUTOFMEMORY 
  
> メモリ不足のため、登録が失敗しました。
    
## <a name="remarks"></a>注釈

フォームビューアーは、フォームの **IMAPIForm::Advise** メソッドを呼び出して、フォームに変更が発生した場合に通知を登録します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

イベントが発生した場合に適切な [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md)メソッドを呼び出す際に使用できるよう _、pAdvise_ パラメーターで渡されたビューアアドバイス シンク ポインターのコピーを保持します。 通知の登録が取り消されるまでポインターを保持するには、ビュー アアドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) メソッドを呼び出します。 _pulConnection パラメーターの内容を_ 0 以外の数値に設定します。 
  
多くのフォームでは、イベントの登録および後続の通知を処理するヘルパー オブジェクトを実装しています。 
  
通知プロセス全般の詳細については [、「MAPI でのイベント通知」を参照してください](event-notification-in-mapi.md)。 
  
通知とフォームの詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MAPI のイベント通知](event-notification-in-mapi.md)
  
[フォーム通知の送受信](sending-and-receiving-form-notifications.md)

