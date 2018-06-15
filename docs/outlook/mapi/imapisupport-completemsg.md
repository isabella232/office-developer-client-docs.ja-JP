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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800729"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**適用されます**: Outlook 
  
メッセージのポスト プロセスを実行します。 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]メッセージを処理するためのエントリの識別子へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 後処理が正常に完了しました。
    
## <a name="remarks"></a>Remarks

**IMAPISupport::CompleteMsg**メソッドは、メッセージ ストア プロバイダーのサポートのオブジェクトに実装されており、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーによってのみ呼び出されます。 密結合のストア プロバイダーは、メッセージをポスト プロセスに MAPI スプーラーに指示するために**IMAPISupport::CompleteMsg**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

トランスポート プロバイダーと密に結合する、すべてのメッセージの受信者を処理することができ、次の条件のいずれかが存在する場合にのみ、 **CompleteMsg**を呼び出します。 
  
- メッセージをプリプロセスされました。
    
- メッセージには、MAPI スプーラーによって後処理が必要です。
    
## <a name="see-also"></a>関連項目



[IMAPISupport: IUnknown](imapisupportiunknown.md)

