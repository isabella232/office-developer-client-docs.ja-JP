---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: personsAddresses パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。
ms.openlocfilehash: 88fef14135718e7b054cf85f7e12bb7b0f9c0478
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629152"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

_personsAddresses_ パラメーターで指定されたユーザーの人物と画像の詳細のコレクションを含む文字列を返します。 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>パラメーター

_personsAddresses_
  
> [in]一連のユーザーのハッシュ化された SMTP アドレスを指定する XML 文字列。
    
_personsCollection_
  
> [out]人物と画像の詳細のコレクションを含む XML 文字列。
    
## <a name="remarks"></a>注釈

この Outlook ソーシャル コネクタ (OSC) は、OSC プロバイダーがフレンドとフレンド以外のオンデマンドまたはハイブリッド同期をサポートしている場合に **GetPeopleDetails** を呼び出します。 
  
_personsAddresses パラメーター_ は、OSC プロバイダーの拡張性のスキーマで定義されている **hashedAddresses** のスキーマ定義に準拠している必要があります。 _personsAddresses 文字列_ は、People Pane に表示される各ユーザーのハッシュ化された SMTP アドレスのセットを表します。 ユーザーは [、ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) プロパティで表されるログオン ユーザーのフレンドである必要があります。 ハッシュされた SMTP アドレスは、プロバイダーの機能 XML の **hashFunction** 要素で指定されたハッシュ関数を **使用して暗号化** されます。 OSC は **、personAddresses** コレクション内の各ハッシュされた  _Addressを index_ 要素で **識別** します。 プロバイダーは **、GetPeopleDetails** のフレンド **XML** を返す際に、index 要素を使用して受信者 **の個人** XML を識別する必要があります。  受信者がソーシャル ネットワーク上の登録ユーザーではない場合、プロバイダーは、その受信者 **の任意の** ユーザー XML を返す必要があります。 ユーザー **XML で** 表される各ネットワークユーザーの index 要素は _、personsAddresses_ の受信者の **index** 要素に対応します。
  
OSC は  _、personsCollection_ パラメーターによって返される情報をメモリに格納します。 _personsCollection_ XML 文字列は、OSC プロバイダーの拡張性のスキーマで定義されているフレンドのスキーマ定義に準拠している必要があります。 OSC がメモリ内でこの情報を使用して更新する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)

