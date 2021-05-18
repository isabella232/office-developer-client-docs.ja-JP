---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406172"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの印刷状態をフォーム ビューアーに通知します。
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>パラメーター

 _dwPageNumber_
  
> [in]印刷された最後のページの番号。
    
 _hrStatus_
  
> [in]印刷ジョブの状態を示す HRESULT 値。 使用可能な値は次のいずれかです。
    
S_FALSE 
  
> 印刷ジョブが正常に終了しました。
    
S_OK 
  
> 印刷ジョブが進行中です。
    
FAILED 
  
> エラーが原因で印刷ジョブが終了しました。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリックして操作をキャンセルしました。 
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **、印刷中に IMAPIViewAdviseSink::OnPrint** メソッドを呼び出して、印刷の進行状況をビューアーに通知します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

印刷ジョブに複数のページが含まれる場合は、各ページの印刷後に **OnPrint** を呼び出します。 _dwPageNumber を_ 現在印刷中のページに設定し _、hrStatus_ を [S_OK. 印刷ジョブが完了したら、印刷された最後のページに _dwPageNumber_ が設定された **OnPrint** を呼び出し _、hrStatus_ を [印刷] にS_FALSE。 
  
フォーム通知の詳細については、「フォーム通知の送受信 [」を参照してください](sending-and-receiving-form-notifications.md)。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

