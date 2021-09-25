---
title: プロファイルの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fc951d5b4a031aed335181ac8534ac4eb9c6c8ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588183"
---
# <a name="deleting-a-profile"></a>プロファイルの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **プロファイルを削除するには**
  
- [IProfAdmin::D Profile を呼び出します](iprofadmin-deleteprofile.md)。
    
 **DeleteProfile は** 、プロファイルが現在使用されている場合は削除のマークを付け、プロファイルの削除がアクティブでなくなるまで待機します。 アクティブなセッションを持つすべてのクライアントが切断されるまで、プロファイルは実際には消えません。 
  
 **DeleteProfile は** 、プロファイル内のすべてのメッセージ サービスのエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターを MSG_SERVICE_DELETE。 エントリ ポイント関数の呼び出しは、サービスがプロファイルから物理的に削除される前に行われます。 
  

