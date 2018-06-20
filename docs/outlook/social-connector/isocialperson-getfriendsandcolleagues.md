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
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804348"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

ユーザーのコレクションを表す文字列を取得します。
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parameters

_personsCollection_
  
> [out]XML 文字列をユーザーの友人のセットを表し、Outlook ソーシャル コネクタ (OSC) プロバイダーの機能拡張用の XML スキーマで定義されている、**友人**の定義に準拠しています。 
    
## <a name="remarks"></a>備考

OSC は、ソーシャル ネットワーク上の**GetFriendsAndColleagues** OSC プロバイダーをサポートしていますがキャッシュされている場合、またはハイブリッドの同期の友人を呼び出します。 OSC 最初にメソッドを呼び出して、 **GetFriendsAndColleagues** **GetFriendsAndColleagues** 、ソーシャル ネットワークにログオンしている Outlook ユーザーのソーシャル ネットワークにログオン中のユーザーの友人を表す XML 文字列を返します。 XML 文字列では、**友人**の XML スキーマ定義に準拠し、各フレンドの**人**の要素 (OSC プロバイダーのスキーマ定義に準拠しても) を指定します。 
  
**GetFriendsAndColleagues**が返されるとき、友人にログオンしたユーザーの情報、OSC は、連絡先フォルダーに情報を格納します。 このフォルダーでは、ソーシャル ネットワークに固有では、ログオンしているユーザーの既定の Outlook ストアに存在します。 OSC が連絡先フォルダー内の友人の情報をキャッシュする方法の詳細については、[同期の友人との活動](synchronizing-friends-and-activities.md)を参照してください。
  
_PersonsCollection_パラメーターで返される各フレンドの情報は、**ユーザー**の XML スキーマ定義に準拠します。 **人**要素情報の多くの部分をサポートして、SMTP 電子メール アドレス ( **emailAddress**、 **emailAddress2**、および**emailAddress3**の要素にマップする) を含む、各フレンドのフレンドを指定する、ソーシャル ネットワーク、および、ユーザー ID (**ユーザー Id**の要素にマップする)、ソーシャル ネットワーク上の友人を識別します。 
  
人物情報ウィンドウで選択されている Outlook のユーザーのアクティビティを表示するには、OSC は、 **GetFriendsAndColleagues**から返されるそれぞれの友人とのユーザーの一致を試みます。 OSC 各友人がソーシャル ネットワークに指定した電子メール アドレスを選択した Outlook のユーザーの SMTP アドレスを照合することによって行われます。 OSC では、一致する SMTP 電子メール アドレスを検出した場合、OSC は[ISocialSession::GetPerson](isocialsession-getperson.md)メソッドを呼び出す、友人の対応する**ユーザー Id**を使用します。 これは、その友人は、ソーシャル ネットワークの活動とその友人の画像を取得するのには OSC を有効にし、 [ISocialPerson](isocialpersoniunknown.md)オブジェクトを取得します。 
  
ただし、選択した Outlook ユーザーは、ソーシャル ネットワーク上のアカウントで同じ SMTP アドレスを指定しない場合、または Outlook のユーザーはソーシャル ネットワークのアカウントを持っていない場合は、OSC ユーザーの一致を検索することはできませんし、activiti は表示されません。es ソーシャル ネットワークのユーザーにします。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson: IUnknown](isocialpersoniunknown.md)
- [フレンド情報の取得](getting-friends-information.md)

