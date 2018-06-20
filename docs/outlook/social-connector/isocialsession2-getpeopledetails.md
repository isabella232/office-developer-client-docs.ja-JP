---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: PersonsAddresses パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804377"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

_PersonsAddresses_パラメーターで指定されたユーザーのユーザーと画像の詳細情報のコレクションを格納する文字列を返します。 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameters

_personsAddresses_
  
> [in]ハッシュ化された一連のユーザーの SMTP アドレスを指定する XML 文字列です。
    
_personsCollection_
  
> [out]人と画像の詳細のコレクションを格納する XML 文字列です。
    
## <a name="remarks"></a>備考

OSC プロバイダー以外の友人や友人のオン ・ デマンドまたはハイブリッドの同期をサポートしている場合、Outlook ソーシャル コネクタ (OSC) は**GetPeopleDetails**を呼び出します。 
  
_PersonsAddresses_パラメーターは、OSC プロバイダーの拡張機能のスキーマで定義されている**hashedAddresses**のスキーマ定義に従う必要があります。 _PersonsAddresses_文字列は、人物情報ウィンドウに表示される各ユーザーの SMTP アドレスをハッシュのセットを表します。 ユーザーは、 [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオン中のユーザーのフレンドではありません。 ハッシュの SMTP アドレスは、プロバイダーの**機能**XML で**実装しています。** 要素で指定するハッシュ関数を使用して暗号化されます。 OSC では、**インデックス**の要素を持つ_personAddresses_コレクション内の各**hashedAddress**を識別します。 プロバイダーは、 **GetPeopleDetails**の**友人**XML が返されるときに、XML の受信者の**ユーザー**を識別するのに**インデックス**の要素を使用する必要があります。 受信者がソーシャル ネットワークに登録されているユーザーでない場合、プロバイダーはその受信者の**人**XML を返さなければなりません。 **人**XML で表されるネットワークのユーザーごとに**インデックス**の要素は、 _personsAddresses_内の受信者の**インデックス**の要素に対応しています。
  
OSC では、メモリ内の_personsCollection_パラメーターによって返される情報を格納します。 _PersonsCollection_ XML 文字列は、OSC プロバイダーの拡張機能のスキーマで定義されている、**友人**のスキーマ定義に従ってください。 OSC を使用してメモリ内には、この情報を更新する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2: IUnknown](isocialsession2iunknown.md)
- [友人や活動を同期します。](synchronizing-friends-and-activities.md)

