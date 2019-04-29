---
title: imapisupportcompletemsg
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番処理するメッセージのエントリ id へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 後処理が正常に完了しました。
    
## <a name="remarks"></a>注釈

**imapisupport::** "は、メッセージストアプロバイダーのサポートオブジェクトに対して実装されており、トランスポートプロバイダーと密接に結合されたメッセージストアプロバイダーのみが呼び出されます。 密結合ストアプロバイダーは、メッセージをポスト処理するように MAPI スプーラーに指示する**imapisupport:: completemsg**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

呼び出し**** の待機は、トランスポートプロバイダーに密接に結合している場合にのみ、すべてのメッセージの受信者を処理でき、次の条件のいずれかが存在することになります。 
  
- メッセージが前処理されました。
    
- このメッセージには、MAPI スプーラーによる後処理が必要です。
    
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

