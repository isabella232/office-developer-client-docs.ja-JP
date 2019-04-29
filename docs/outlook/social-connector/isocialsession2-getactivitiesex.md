---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: hashedAddresses パラメーターによって指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404338"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

_hashedAddresses_パラメーターによって指定された各ユーザーのアクティビティのコレクションを表す文字列を取得します。 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>パラメーター

_hashedAddresses_
  
> 順番一連のユーザーのハッシュ化された SMTP アドレスの配列を指定する構造体。
    
_startTime_
  
> 順番作成されたアクティビティが返されるまでの時間。
    
_アクティビティ_
  
> 読み上げ_startTime_以降にソーシャルネットワーク上の_hashedAddresses_によって指定されたユーザーのアクティビティのセットを表す XML 文字列。
    
## <a name="remarks"></a>注釈

.osc プロバイダーがアクティビティのオンデマンド同期をサポートしている場合、.osc 呼び出しは**GetActivitiesEx**です。 .osc は、_アクティビティ_で返された情報をメモリに格納します。 .osc がメモリでこの情報を使用して更新する方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。
  
Outlook Social Connector 2013 以降では、アクティビティのオンデマンド同期のみをサポートし、 **GetActivitiesEx**のみを呼び出してアクティビティを取得します。 オンデマンドアクティビティ検索をサポートするには、 **cacheactivities**を**false**に、 **getactivities**と**dynamicActivitiesLookupEx**を**true**として設定し、.osc は**GetActivitiesEx**を呼び出します。
  
返される XML 文字列は、プロバイダ拡張機能のスキーマで定義されているように、 **activityfeed**のスキーマ定義に準拠している必要があります。
  
_hashedAddresses_ sring は、People ウィンドウに表示される各ユーザーの一連のハッシュアドレスを表します。 ハッシュされた SMTP アドレスは、プロバイダーの**機能**XML の**hashfunction**要素によって指定されたハッシュ関数を使用して暗号化されます。 ユーザーは、 [iLoggedOnUserName](isocialsession-loggedonusername.md)プロパティによって表されるログオンユーザーのフレンドである必要はありません。 
  
_startTime_パラメーターは、世界協定時刻 (UTC) の**日付**値です。 現地時刻の値を UTC**日付**の値に変換する必要があります。 
  
**GetActivitiesEx**メソッドが返すアクティビティは、**開始**時刻の値が_startTime_よりも大きく、またはそれより小さいか等しい必要があります。 **startTime**間で変更が行われて**** いない場合、プロバイダーは OSC_E_NO_CHANGES エラーを返す必要があります。
  
## <a name="see-also"></a>関連項目

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)

