---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c21c61f886a6fcc493a83e0af54f010090e2dd3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561461"
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

