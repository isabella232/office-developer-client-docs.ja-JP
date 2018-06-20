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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f3642c890c3922611d57dea6f03aca5606876864
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800815"
---
# <a name="imapisupportstatusrecips"></a>IMAPISupport::StatusRecips

  
  
**適用されます**: Outlook 
  
配信し、配信不能レポートを生成します。
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in]レポートを生成する対象のメッセージへのポインター。
    
 _lpRecipList_
  
> [in]_LpMessage_が指すメッセージの受信者を記述する[ADRLIST](adrlist.md)構造体へのポインターです。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> レポートが正常に生成されました。
    
MAPI_W_ERRORS_RETURNED 
  
> 呼び出しは完了しましたが、この種類の受信者の受信者のオプションはありません。 この警告が返されると、呼び出しを成功として処理する必要があります。 この警告をテストするには、 **HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
    
## <a name="remarks"></a>備考

トランスポート プロバイダーのサポート オブジェクトの**IMAPISupport::StatusRecips**メソッドを実装します。 トランスポート プロバイダーは、その MAPI の送信を要求する**StatusRecips**の 1 つまたは複数のメッセージの受信者に配信または配信不能レポートを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージの処理中には、 **StatusRecips**を複数回呼び出すことができます。 ただし、開いているメッセージの**StatusRecips**を呼び出すと場合、は、メッセージの受信者のすべての配信と配信不能の情報を収集し、その受信者のリストに**StatusRecips**を呼び出して、最善を行います。 コレクションの 1 つのポイントは重要ですが、1 人の受信者に複数の**StatusRecips**呼び出しで複数の同じレポートが送信されます。 
  
メッセージの配信または_lpRecipList_パラメーターで指定された**ADRLIST**構造体で配信不能に関連するプロパティを格納します。 配信レポートと配信不能レポートの必須およびオプションのプロパティの一覧は、[必要なレポートのメッセージのプロパティ](required-report-message-properties.md)と[オプションのレポート メッセージのプロパティ](optional-report-message-properties.md)を参照してください。 
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)と[MAPIAllocateMore](mapiallocatemore.md)関数を使用して、 _lpRecipList_の**ADRLIST**構造体のメモリを割り当てます。 MAPI は、関数を呼び出して、 [MAPIFreeBuffer](mapifreebuffer.md) **StatusRecips**が成功した場合にのみメモリを解放します。 
  
配信し、配信不能レポートの概要については、 [MAPI レポート メッセージ](mapi-report-messages.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[ADRLIST](adrlist.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

