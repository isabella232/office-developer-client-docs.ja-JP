---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411191"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージに対して後処理を実行します。 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]処理するメッセージのエントリ識別子へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 後処理が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::CompleteMsg** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装され、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーによってのみ呼び出されます。 緊密に結合されたストア プロバイダーは **IMAPISupport::CompleteMsg** を呼び出して、MAPI スプーラーにメッセージの後処理を指示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**CompleteMsg の** 呼び出しは、トランスポート プロバイダーと緊密に結合されている場合にのみ、メッセージのすべての受信者を処理できます。次のいずれかの条件が存在します。 
  
- メッセージが前処理されました。
    
- メッセージには、MAPI スプーラーによる後処理が必要です。
    
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

