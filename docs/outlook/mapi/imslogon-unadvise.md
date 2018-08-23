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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4ee17799fc42faf383461af7eed9d700d17b868e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582386"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
[IMSLogon::Advise](imslogon-advise.md)メソッドへの呼び出しを使用して、以前に確立されたメッセージ ストアの変更を通知するためのオブジェクトの登録を削除します。 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulConnection_
  
> [in]**IMSLogon::Advise**への呼び出しによって返された登録接続の数です。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージ ストア プロバイダーの実装**IMSLogon::Advise**、それによって通知をキャンセルするのには、以前の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズ シンク オブジェクトへのポインターを解放する**IMSLogon::Unadvise**メソッド登録します。 アドバイズ シンク オブジェクトへのポインターを破棄することの一環として、オブジェクト[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)呼び出されます。 一般に、**リリース**と呼ばれる**Unadvise**の呼び出し中にします。 ただし、別のスレッドがアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。 
  
## <a name="see-also"></a>関連項目



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

