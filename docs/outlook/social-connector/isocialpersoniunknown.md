---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: ソーシャル ネットワーク上のユーザーを表します。
ms.openlocfilehash: ab2182a78f87cb32706a11d13f970f18e635cf6a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590444"
---
# <a name="isocialperson--iunknown"></a>ISocialPerson : IUnknown

ソーシャル ネットワーク上のユーザーを表します。
  
## <a name="members"></a>メンバー

次の表に **、ISocialPerson** インターフェイスで使用できるメンバーを示します。 
  
|**名前**|**メンバーの種類**|**説明**|
|:-----|:-----|:-----|
|[GetActivities](isocialperson-getactivities.md) <br/> |Method  <br/> |このメソッドは、ソーシャル コネクタ 2013 Outlook廃止されました。  <br/> |
|[GetDetails](isocialperson-getdetails.md) <br/> |Method  <br/> |名、名、プロファイル画像の URL など、人物の詳細を表す文字列を取得します。  <br/> |
|[GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) <br/> |Method  <br/> |ユーザーのコレクションを表す文字列を取得します。  <br/> |
|[GetFriendsAndColleaguesIDs](isocialperson-getfriendsandcolleaguesids.md) <br/> |Method  <br/> |このメソッドは現在サポートされていません。  <br/> |
|[GetPicture](isocialperson-getpicture.md) <br/> |Method  <br/> |ユーザーのピクチャ リソースを含むバイトの配列を取得します。  <br/> |
|[GetStatus](isocialperson-getstatus.md) <br/> |Method  <br/> |このメソッドは現在サポートされていません。  <br/> |
   
## <a name="remarks"></a>注釈

ソーシャル Outlook (OSC) プロバイダーは、OSC と通信するためにこのインターフェイスを実装する必要があります。
  
## <a name="see-also"></a>関連項目

- [Outlookソーシャル コネクタ プロバイダー インターフェイス](outlook-social-connector-provider-interfaces.md)

