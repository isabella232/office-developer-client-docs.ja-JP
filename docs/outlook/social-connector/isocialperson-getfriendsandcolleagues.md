---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: ユーザーのコレクションを表す文字列を取得します。
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407656"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

ユーザーのコレクションを表す文字列を取得します。
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>パラメーター

_personsCollection_
  
> [out]ユーザーのフレンドのセットを表し、Outlook Social Connector (OSC) プロバイダーの機能拡張の XML スキーマで定義されているフレンドの定義に準拠する XML 文字列。 
    
## <a name="remarks"></a>注釈

OSC プロバイダーがソーシャル ネットワーク上の友人のキャッシュまたはハイブリッド同期をサポートしている場合、OSC は **GetFriendsAndColleagues** を呼び出します。 OSC が最初に、ソーシャル ネットワークにログオンしている Outlook ユーザーの **GetFriendsAndColleagues** メソッドを呼び出す場合 **、GetFriendsAndColleagues** は、ソーシャル ネットワーク上でログオンしているユーザーの友人を表す XML 文字列を返します。 XML 文字列はフレンド **XML** スキーマ定義に準拠し、各フレンドの person 要素 (OSC プロバイダー スキーマ定義にも準拠) を指定します。 
  
**GetFriendsAndColleagues** がログオンしているユーザーのフレンド情報を返す場合、OSC は連絡先フォルダーにその情報を格納します。 このフォルダーはソーシャル ネットワークに固有のフォルダーで、ログオンしているユーザーの既定のユーザー ストアにOutlookされます。 OSC が連絡先フォルダーに友人の情報をキャッシュする方法の詳細については、「友人とアクティビティの同期」 [を参照してください](synchronizing-friends-and-activities.md)。
  
_personsCollection_ パラメーターで返される各フレンドの情報は、ユーザーの XML スキーマ定義に準拠 **しています**。 person要素は、フレンドがソーシャル ネットワークで指定した SMTP メール アドレス (emailAddress、emailAddress2、emailAddress3 要素にマップされる) や、ソーシャル ネットワーク上のそのフレンドを識別するユーザー ID **(userID** 要素にマップされる) など、各フレンドの多くの情報をサポートします。    
  
ユーザー ウィンドウで選択された Outlook ユーザーのアクティビティを表示するには、OSC は **GetFriendsAndColleagues** から返された各フレンドとユーザーの一致を試行します。 OSC は、選択したユーザーの SMTP アドレスOutlook、各フレンドがソーシャル ネットワークで指定した電子メール アドレスと照合します。 OSC が一致する SMTP 電子メール アドレスを見つけた場合、OSC はフレンドの対応する **userID** を使用して [ISocialSession::GetPerson](isocialsession-getperson.md) メソッドを呼び出します。 これは、そのフレンドの [ISocialPerson](isocialpersoniunknown.md) オブジェクトを取得するために行います。これにより、OSC はソーシャル ネットワークからその友人のアクティビティと写真を取得できます。 
  
ただし、選択した Outlook ユーザーがソーシャル ネットワーク上のアカウントで同じ SMTP アドレスを指定しない場合、または Outlook ユーザーがそのソーシャル ネットワーク上のアカウントを持ってない場合、OSC は、そのユーザーに一致する一致を見つけ、そのユーザーのアクティビティをソーシャル ネットワーク上に表示しません。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [フレンド情報の取得](getting-friends-information.md)

