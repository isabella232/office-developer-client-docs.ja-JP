---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: emailAddresses パラメーターと displayName パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。
ms.openlocfilehash: 6da454bb1c913951b492b8e6f4c63af9178134d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608821"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

_emailAddresses_ パラメーターと _displayName_ パラメーターで識別されるユーザーを、ソーシャル ネットワーク上のログオンユーザーのフレンドとして追加します。 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>パラメーター

_emailAddresses_
  
> [in]ソーシャル ネットワーク上のユーザーの有効な SMTP アドレスを 1 つ以上含む配列。
    
_displayName_
  
> [in]フレンドとして追加するユーザーの表示名を含む文字列。
    
## <a name="remarks"></a>注釈

Outlook ソーシャル コネクタ (OSC) が **emailAddresses** パラメーターの配列内の SMTP アドレスよりも多くを提供する場合、OSC プロバイダーは、最初の要素がプライマリ SMTP アドレスと見なされます。 
  
プロバイダーが、機能 **XML** で **followPerson** 要素を true に設定し _、emailAddresses_ の要素のいずれもネットワーク上のユーザーと一致しない場合、プロバイダーは OSC_E_NOT_FOUND エラーを返す必要があります。  プロバイダーが **followPerson** を機能で **false** に設定している場合、プロバイダーはエラー メッセージをOSC_E_FAILします。 
  
**FollowPersonEx** メソッドが成功した場合、プロバイダーは _displayName_ パラメーターの文字列を使用して、そのユーザーに SMTP アドレスでアドレス指定するのではなく、後続のフレンド確認メールのユーザーにアドレスを指定できます。 一方、プロバイダーは displayName パラメーターに空の文字列を渡す OSC を  _処理できる必要_ があります。 
  
プロバイダーが [ISocialSession2](isocialsession2iunknown.md)インターフェイスを実装し、機能 XML で **followPerson** を **true** に設定している場合、OSC は [ISocialSession::FollowPerson](isocialsession-followperson.md)の代わりに **FollowPersonEx** を呼び出します。 プロバイダーが **followPerson** をtrue に設定しているが **、ISocialSession2** インターフェイスを実装していない場合、または **FollowPersonEx** が OSC_E_NOTIMPL エラーを返す場合、OSC は **ISocialSession::FollowPerson** を呼び出します。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

