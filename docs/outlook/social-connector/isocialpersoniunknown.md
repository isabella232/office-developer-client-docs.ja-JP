---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: ソーシャル ネットワーク上のユーザーを表します。
ms.openlocfilehash: d6fca18ac2d2074239bd8b435bcd40971de83670
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804350"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

ソーシャル ネットワーク上のユーザーを表します。
  
## <a name="members"></a>Members

次の表は、 **ISocialPerson**インターフェイスで使用可能なメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |メソッド  <br/> |Outlook ソーシャル コネクタ 2013 以降、このメソッドは廃止されました。  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |メソッド  <br/> |プロフィールの画像に、名、姓、名、URL など、個人の詳細情報を表す文字列を取得します。  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |メソッド  <br/> |ユーザーのコレクションを表す文字列を取得します。  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |メソッド  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |メソッド  <br/> |個人の画像リソースを格納するバイトの配列を取得します。  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |メソッド  <br/> |このメソッドは現在サポートされていません。  <br/> |
   
## <a name="remarks"></a>注釈

Outlook ソーシャル コネクタ (OSC) プロバイダーには、OSC と通信するには、このインターフェイスを実装しなければなりません。
  
## <a name="see-also"></a>関連項目

- [Outlook ソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

