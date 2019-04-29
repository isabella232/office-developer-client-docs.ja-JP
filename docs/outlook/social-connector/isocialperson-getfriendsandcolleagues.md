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

_個人コレクション_
  
> 読み上げ個人のフレンドのセットを表す xml 文字列。 Outlook Social Connector (.osc) プロバイダー拡張機能の XML スキーマで定義されているように、**フレンド**の定義に準拠しています。 
    
## <a name="remarks"></a>注釈

.osc プロバイダーがソーシャルネットワーク上で友人のキャッシュまたはハイブリッド同期をサポートしている場合、.osc 呼び出しは**GetFriendsAndColleagues**になります。 ソーシャルネットワークにログオンしている Outlook ユーザーの**GetFriendsAndColleagues**メソッドを最初に呼び出すときに、 **GetFriendsAndColleagues**は、ソーシャルネットワーク上でログオンしているユーザーのフレンドを表す XML 文字列を返します。 xml 文字列は、フレンド xml **** スキーマ定義に準拠しており、各フレンドの**person**要素 (.osc プロバイダースキーマ定義にも準拠) を指定します。 
  
**GetFriendsAndColleagues**がログオンユーザーのフレンド情報を返すと、.osc は連絡先フォルダーにその情報を格納します。 このフォルダーは、ソーシャルネットワークに固有のものであり、ログオンしているユーザーの既定の Outlook ストアに存在します。 .osc が連絡先フォルダー内のフレンド情報をキャッシュする方法の詳細については、「[友人とアクティビティを同期](synchronizing-friends-and-activities.md)する」を参照してください。
  
個人_コレクション_パラメーターに返される各フレンドの情報は、 **person**の XML スキーマ定義に準拠しています。 **person**要素は、各フレンドの多くの情報 ( **emailAddress**、 **emailAddress2**、および**emailAddress3**要素にマップされる) をサポートしており、その中で友人が指定したソーシャルネットワークと、ソーシャルネットワーク上でその友人を識別するユーザー ID ( **userID**要素にマップされます)。 
  
[ユーザー] ウィンドウで選択された Outlook ユーザーのアクティビティを表示するために、.osc は、 **GetFriendsAndColleagues**から返された各フレンドに対してユーザーを照合しようとします。 .osc は、選択された Outlook ユーザーの SMTP アドレスを、各フレンドがソーシャルネットワーク上で指定した電子メールアドレスと照合することによって、これを行います。 一致する SMTP 電子メールアドレスを、.osc が検出した場合、.osc はフレンドの対応する**userID**を使用して、 [isocialsession:: getperson](isocialsession-getperson.md)メソッドを呼び出します。 これにより、そのフレンドの[isocial alperson](isocialpersoniunknown.md)オブジェクトが取得されます。これにより、.osc がその友人のアクティビティと画像をソーシャルネットワークから取得できるようになります。 
  
ただし、選択した outlook ユーザーがソーシャルネットワーク上のアカウントで同じ SMTP アドレスを指定していない場合、または outlook ユーザーがそのソーシャルネットワークにアカウントを持っていない場合、そのユーザーに対して一致するものを検索することができず、activiti が表示されません。そのユーザーのソーシャルネットワーク上での es。
  
## <a name="see-also"></a>関連項目

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [フレンド情報の取得](getting-friends-information.md)

