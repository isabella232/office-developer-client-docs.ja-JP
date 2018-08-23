---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: HashedAddresses パラメーターで指定されたユーザーのそれぞれの活動のコレクションを表す文字列を取得します。
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804375"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

_HashedAddresses_パラメーターで指定されたユーザーのそれぞれの活動のコレクションを表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>パラメーター

_hashedAddresses_
  
> [in]ハッシュされた SMTP の配列を指定する構造体は、一連のユーザーに対応します。
    
_開始時刻_
  
> [in]作成された活動項目が返されますになる時間です。
    
_アクティビティ_
  
> [out]_開始時刻_以降に、ソーシャル ネットワーク上の_hashedAddresses_で指定されたユーザーのアクティビティのセットを表す XML 文字列です。
    
## <a name="remarks"></a>注釈

OSC は、OSC プロバイダーには、活動のオン ・ デマンドの同期がサポートされている場合に**GetActivitiesEx**を呼び出します。 OSC では、メモリ内_のアクティビティ_に返される情報を格納します。 OSC を使用してメモリ内には、この情報を更新する方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。
  
Outlook ソーシャル コネクタ 2013 で開始、OSC はだけオンデマンド同期アクティビティをサポートし、活動を取得するのには**GetActivitiesEx**を呼び出します。 オンデマンド アクティビティの参照をサポートするには、 **false**、および**getActivities**と**真**の**dynamicActivitiesLookupEx**と、OSC に**GetActivitiesEx**を呼び出すと**cacheActivities**を設定します。
  
返される XML 文字列は、OSC プロバイダーの拡張機能のスキーマで定義されている**activityFeed**のスキーマ定義に従う必要があります。
  
_HashedAddresses_ sring では、人物情報ウィンドウに表示される各ユーザーのハッシュ化されたアドレスのセットを表します。 ハッシュの SMTP アドレスは、プロバイダーの**機能**XML で**実装しています。** 要素で指定するハッシュ関数を使用して暗号化されます。 ユーザーは、 [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオン中のユーザーのフレンドではありません。 
  
_開始時刻_パラメーターは、世界協定時刻 (UTC) で**日付**値です。 現地時刻の値は、UTC**の日付**値に変換しなければなりません。 
  
**GetActivitiesEx**メソッドが返すアクティビティの作成時刻の値、_開始時刻_よりも大きい必要があり、**今すぐ**に小さい。 **開始時刻**と**現在**の間で変更が発生していない、プロバイダーは、OSC_E_NO_CHANGES エラーを返す必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [友人や活動を同期します。](synchronizing-friends-and-activities.md)

