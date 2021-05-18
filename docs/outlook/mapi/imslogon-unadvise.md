---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317277"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMSLogon::Advise](imslogon-advise.md)メソッドの呼び出しを使用して、以前に確立されたメッセージ ストアの変更の通知に対するオブジェクトの登録を削除します。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in] **IMSLogon::Advise** の呼び出しによって返される登録接続の数。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは **、IMSLogon::Unadvise** メソッドを実装して、前の **IMSLogon::Advise** の呼び出しで _lpAdviseSink_ パラメーターで渡されたアアドバイス シンク オブジェクトへのポインターを解放し、通知登録を取り消します。 アアドバイス シンク オブジェクトへのポインターを破棄する一環として、オブジェクトの [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) メソッドが呼び出されます。 通常、 **リリースは** **Unadvise 呼び出し中に呼び出** されます。 ただし、別のスレッドが、アドバイス シンク オブジェクト [の IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す過程にある場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

