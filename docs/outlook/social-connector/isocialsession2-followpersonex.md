---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: emailaddresses および displayName パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429832"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

_emailaddresses_および_displayName_パラメーターで指定された人物を、ソーシャルネットワーク上のログオンユーザーのフレンドとして追加します。 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>パラメーター

_emailAddresses_
  
> 順番ソーシャルネットワーク上の個人の1つまたは複数の有効な SMTP アドレスが格納された配列。
    
_displayName_
  
> 順番フレンドとして追加する人物の表示名を含む文字列。
    
## <a name="remarks"></a>注釈

Outlook Social Connector (.osc) が**emailaddresses**パラメーターの配列内の SMTP アドレスよりも多い場合、.osc プロバイダーは最初の要素がプライマリ SMTP アドレスであると見なすことができます。 
  
プロバイダーが [**機能**] XML **** で [ **true** ] に設定されている場合、_電子メールアドレス_のどの要素もネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。 プロバイダーが**権限**で OSC_E_FAIL **** を**false**として設定している場合、プロバイダーはエラーを返す必要があります。 
  
このメソッド**** が正常に実行された場合、プロバイダーは_displayName_パラメーターの文字列を使用して、SMTP アドレスでその人物にアドレス指定するのではなく、その人物に対して任意のフレンドリな確認メールを送信することができます。 一方、プロバイダーは、 _displayName_パラメーターに空の文字列を渡して、.osc を処理できる必要があります。 
  
プロバイダーが[ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装していて**** 、capabilities XML に**true**として設定されて**** いる場合、.osc は、 [i alsession::](isocialsession-followperson.md)という形式ではなく、次のようにします。 プロバイダーが**true**とし**** て**ISocialSession2**インターフェイスを実装していない場合、または**** OSC_E_NOTIMPL エラーが発生した場合、.osc は**i alsession::** という名前を呼び出します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

