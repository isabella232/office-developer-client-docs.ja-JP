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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328785"
---
# <a name="imapiviewadvisesinkonprint"></a>IMAPIViewAdviseSink::OnPrint

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームの印刷状態をフォームビューアーに通知します。
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a>パラメーター

 _dwpagenumber_
  
> 順番印刷された最後のページの番号を指定します。
    
 _hrstatus_
  
> 順番印刷ジョブの状態を示す HRESULT 値。 使用可能な値は次のいずれかです。
    
S_FALSE 
  
> 印刷ジョブが正常に終了しました。
    
S_OK 
  
> 印刷ジョブが進行中です。
    
フェール 
  
> 印刷ジョブは失敗したため、終了しました。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知に成功しました。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの [キャンセル] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

フォームオブジェクトは印刷中に**IMAPIViewAdviseSink:: OnPrint**メソッドを呼び出して、印刷の進行状況を表示します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

印刷ジョブに複数のページが含まれている場合は、各ページが印刷された後に、 **OnPrint**を呼び出すことができます。 現在__ 印刷中のページと_hrstatus_を S_OK に設定します。 印刷ジョブが完了すると、 _dwpagenumber_を使用して**OnPrint**を呼び出し、最後のページが印刷され、 _hrstatus_が S_FALSE に設定されます。 
  
フォーム通知の詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

