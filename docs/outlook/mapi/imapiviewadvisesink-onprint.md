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
ms.openlocfilehash: bf3eee43a70fbc4abf32b60379fc7b191bd9d513
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800858"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**適用対象**: Outlook 
  
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

