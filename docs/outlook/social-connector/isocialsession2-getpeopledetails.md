---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返します。
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404534"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

ユーザーの個人情報および画像の詳細のコレクションが含まれている文字列を返し__ ます。 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>パラメーター

_個人住所_
  
> 順番一連のユーザーのハッシュ化された SMTP アドレスを指定する XML 文字列。
    
_個人コレクション_
  
> 読み上げ個人および画像の詳細のコレクションを含む XML 文字列。
    
## <a name="remarks"></a>注釈

.osc プロバイダーが友人および友人以外の**GetPeopleDetails**またはハイブリッド同期をサポートしている場合、Outlook Social Connector (.osc) はを呼び出します。 
  
_個人住所_パラメーターは、プロバイダ拡張機能のスキーマで定義されているように、 **hashedAddresses**のスキーマ定義に準拠している必要があります。 _個人_情報の文字列は、[人] ウィンドウに表示される各ユーザーのハッシュされた SMTP アドレスのセットを表します。 ユーザーは、 [iLoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオンユーザーのフレンドである必要はありません。 ハッシュされた SMTP アドレスは、プロバイダーの**機能**XML の**hashfunction**要素によって指定されたハッシュ関数を使用して暗号化されます。 .osc は、**キーワード**要素を使用して、_個人住所_コレクション内の各**hashedAddress**を識別します。 プロバイダーは、 **GetPeopleDetails**の**フレンド**xml を返すときに、受信者の**person** xml を識別するために、 **index**要素を使用する必要があります。 受信者がソーシャルネットワーク上の登録済みユーザーではない場合、プロバイダーはその受信者の**個人**XML を返さないようにする必要があります。 **person** XML で表される各ネットワークユーザーの**index**要素は、個人_住所_の受信者の**index**要素に対応します。
  
.osc は、_個人コレクション_パラメーターによって返される情報をメモリに格納します。 _個人コレクション_XML 文字列は、プロバイダ拡張機能のスキーマで定義されているように、**フレンド**のスキーマ定義に準拠している必要があります。 .osc がメモリでこの情報を使用して更新する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)

