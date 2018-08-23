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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 202d461d4acefe18e69b47db9319cb328c61406e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592319"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム ビューアーのフォームの印刷の状態を通知します。
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>パラメーター

 _dwPageNumber_
  
> [in]最後のページ数が印刷されます。
    
 _hrStatus_
  
> [in]印刷ジョブのステータスを示す HRESULT 値です。 使用可能な値は次のとおりです。
    
S_FALSE 
  
> 印刷ジョブが正常に完了しました。
    
S_OK 
  
> 印刷ジョブは処理中です。
    
失敗しました。 
  
> 印刷ジョブが失敗したため終了しました。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が成功しました。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [キャンセル] ボタンをクリックするとします。 
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、ビューアーの印刷の進行状況を通知するために印刷中に**IMAPIViewAdviseSink::OnPrint**メソッドを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

印刷ジョブには、複数のページが含まれている場合は、各ページを印刷した後に**OnPrint**を呼び出すことができます。 S_OK を現在印刷中のページに_dwPageNumber_と_hrStatus_を設定します。 印刷ジョブが完了すると、最後の印刷のページを設定する_dwPageNumber_では、**印刷時**の呼び出しおよび_hrStatus_は S_FALSE に設定します。 
  
フォームの通知の詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

