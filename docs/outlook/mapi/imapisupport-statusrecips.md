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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408769"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
配信レポートと配信以外のレポートを生成します。
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]レポートを生成するメッセージへのポインター。
    
 _lpRecipList_
  
> [in]_lpMessage_ が指すメッセージの受信者を表す [ADRLIST](adrlist.md)構造体へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> レポートが正常に生成されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは全体的に成功しましたが、この種類の受信者の受信者オプションはありません。 この警告が返されると、呼び出しは正常に処理されます。 この警告をテストするには、次のマクロ **HR_FAILED** します。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
    
## <a name="remarks"></a>注釈

**IMAPISupport::StatusRecips** メソッドは、トランスポート プロバイダーのサポート オブジェクトに実装されます。 トランスポート プロバイダーは **StatusRecips** を呼び出して、MAPI がメッセージの 1 つ以上の受信者のセットに配信レポートまたは配信不能レポートを送信する要求を行います。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの処理 **中に StatusRecips** を複数回呼び出す場合があります。 ただし、開いているメッセージの **StatusRecips** を呼び出す場合は、メッセージ受信者のすべての配信情報と配信不能情報を収集し、その受信者リストの **StatusRecips** を呼び出してください。 1 つの受信者に対して複数の **StatusRecips** 呼び出しを実行すると、複数の同一のレポートが送信される可能性があるため、コレクションの 1 つのポイントが重要です。 
  
_lpRecipList_ パラメーターで示される **ADRLIST** 構造体のメッセージ配信または配信不能に関連するプロパティを格納します。 配信レポートと配信以外のレポートに必要なプロパティとオプションのプロパティの完全な一覧[](required-report-message-properties.md)については、「必須レポート メッセージのプロパティ」および「オプションのレポート メッセージのプロパティ」[を参照してください](optional-report-message-properties.md)。 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)関数と [MAPIAllocateMore](mapiallocatemore.md)関数を使用して _、lpRecipList_ の **ADRLIST** 構造体のメモリを割り当てる。 MAPI は **、StatusRecips** が成功した場合にのみ [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによってメモリを解放します。 
  
配信レポートと配信以外のレポートの概要については、「MAPI レポート [メッセージ」を参照してください](mapi-report-messages.md)。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

