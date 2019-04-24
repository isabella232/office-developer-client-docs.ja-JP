---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341770"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配信レポートおよび配信不能レポートを生成します。
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番レポートを生成するメッセージへのポインター。
    
 _lpRecipList_
  
> 順番_lpmessage_によって示されるメッセージの受信者を記述する[adrlist](adrlist.md)構造体へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> レポートが正常に生成されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、この種類の受信者のオプションはありません。 この警告が返された場合、呼び出しは正常に処理されます。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
    
## <a name="remarks"></a>解説

**imapisupport:: StatusRecips**メソッドは、トランスポートプロバイダーのサポートオブジェクトに実装されています。 トランスポートプロバイダーは、 **StatusRecips**を呼び出して、MAPI がメッセージの1つ以上の受信者に対して配信レポートまたは配信不能レポートを送信するよう要求します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**StatusRecips**は、メッセージの処理中に複数回呼び出すことができます。 ただし、開いているメッセージに対して**StatusRecips**を呼び出す場合は、メッセージの受信者のすべての配信および配信情報を収集し、その受信者リストの**StatusRecips**を呼び出すことをお勧めします。 1つの受信者に対して複数の**StatusRecips**呼び出しを行うと、複数の同一のレポートが送信される可能性があるため、単一のコレクションのポイントが重要です。 
  
_lpRecipList_パラメーターによって示される**adrlist**構造で、メッセージ配信または配信不能に関連するプロパティを格納します。 配信レポートと配信不能レポートの必須およびオプションのプロパティの完全な一覧については、「[必須のレポートメッセージのプロパティ](required-report-message-properties.md)」および「[オプションのレポートメッセージのプロパティ](optional-report-message-properties.md)」を参照してください。 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して、 _lpRecipList_の**adrlist**構造のメモリを割り当てます。 MAPI では、 **StatusRecips**が正常に終了した場合にのみ[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによってメモリが解放されます。 
  
配信レポートと配信不能レポートの概要については、「 [MAPI レポートメッセージ](mapi-report-messages.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

