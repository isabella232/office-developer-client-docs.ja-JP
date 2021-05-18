---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: hashedAddresses パラメーターで指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404338"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

_hashedAddresses_ パラメーターで指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>パラメーター

_hashedAddresses_
  
> [in]一連のユーザーのハッシュ化された SMTP アドレスの配列を指定する構造体。
    
_startTime_
  
> [in]作成されたアクティビティが返される時間。
    
_activities_
  
> [out]_startTime_ 以降のソーシャル ネットワーク上の _hashedAddresses_ で指定されたユーザーのアクティビティのセットを表す XML 文字列です。
    
## <a name="remarks"></a>注釈

OSC プロバイダーがアクティビティのオンデマンド同期をサポートしている場合、OSC は **GetActivitiesEx** を呼び出します。 OSC は、アクティビティに返される情報を  _メモリに_ 格納します。 OSC がメモリ内でこの情報を使用して更新する方法の詳細については、「友人とアクティビティの同期 [」を参照してください](synchronizing-friends-and-activities.md)。
  
Outlook Social Connector 2013 から、OSC はアクティビティのオンデマンド同期のみをサポートし、アクティビティを取得するために **GetActivitiesEx** のみを呼び出します。 オンデマンド アクティビティの参照をサポートするには **、cacheActivities** **を** false に設定し **、getActivities および dynamicActivitiesLookupEx** を **true** に設定し、OSC は **GetActivitiesEx** を呼び出します。 
  
返される XML 文字列は、OSC プロバイダーの機能拡張のスキーマで定義されている **activityFeed** のスキーマ定義に準拠している必要があります。
  
_hashedAddresses sring_ は、People Pane に表示される各ユーザーのハッシュされたアドレスのセットを表します。 ハッシュされた SMTP アドレスは、プロバイダーの機能 XML の **hashFunction** 要素で指定されたハッシュ関数を **使用して暗号化** されます。 ユーザーは [、ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) プロパティで表されるログオン ユーザーのフレンドである必要があります。 
  
_startTime パラメーター_ は、**協定世界時**(UTC) の Date 値です。 現地時間の値は UTC 日付値に **変換する必要** があります。 
  
**GetActivitiesEx** メソッドが返すアクティビティには _、startTime_ より大きく、Now 以下の作成時間値が必要 **です**。 **startTime** と Now の間に変更が発生した **場合、プロバイダー** はエラーメッセージをOSC_E_NO_CHANGESがあります。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)

