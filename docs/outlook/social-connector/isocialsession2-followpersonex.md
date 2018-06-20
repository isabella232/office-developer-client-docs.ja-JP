---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: ソーシャル ネットワークにログオン中のユーザーのフレンドとして、emailAddresses パラメーターと displayName パラメーターで識別されるユーザーを追加します。
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804382"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

ソーシャル ネットワークにログオン中のユーザーのフレンドとして、 _emailAddresses_パラメーターと_displayName_パラメーターで識別されるユーザーを追加します。 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parameters

_emailAddresses_
  
> [in]ソーシャル ネットワーク上のユーザーの 1 つまたは複数の有効な SMTP アドレスを含む配列です。
    
_displayName_
  
> [in]友人として追加するユーザーの表示名を含む文字列です。
    
## <a name="remarks"></a>備考

Outlook ソーシャル コネクタ (OSC) は、多くの場合よりも OSC プロバイダー、 **emailAddresses**パラメーターの配列内の SMTP アドレスの最初の要素は、プライマリ SMTP アドレスと仮定できます。 
  
プロバイダーは**機能**XML で**は** **followPerson**要素を設定するには、ネットワーク上のユーザーが一致する_emailAddresses_の要素がない場合、プロバイダーは、OSC_E_NOT_FOUND エラーを返す必要があります。 設定した場合、プロバイダー **followPerson** **false**として**の機能**で、プロバイダーは、OSC_E_FAIL エラーを返す必要があります。 
  
**FollowPersonEx**メソッドが成功した場合、プロバイダー文字列を使用できます、 _displayName_パラメーターで SMTP アドレスを使用してユーザーをアドレス指定するのではなく、その後友人に確認の電子メールでユーザーに対応します。 その一方で、プロバイダーがあります OSC の_displayName_パラメーターに空の文字列を渡すことを処理するために。 
  
プロバイダーは、 [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装するし、 **true**では、XML の機能として**followPerson**を設定するには、OSC は、 [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに**FollowPersonEx**を呼び出します。 プロバイダーは、 **true**として**followPerson**を設定しましたが、 **ISocialSession2**インターフェイスを実装しません、 **FollowPersonEx**が OSC_E_NOTIMPL のエラーを返す場合、OSC は**ISocialSession::FollowPerson**を呼び出します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)

