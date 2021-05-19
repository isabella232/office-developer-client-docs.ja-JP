---
title: プロファイルの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410204"
---
# <a name="deleting-a-profile"></a>プロファイルの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **プロファイルを削除するには**
  
- [IProfAdmin::D Profile を呼び出します](iprofadmin-deleteprofile.md)。
    
 **DeleteProfile は** 、プロファイルが現在使用されている場合は削除のマークを付け、プロファイルの削除がアクティブでなくなるまで待機します。 アクティブなセッションを持つすべてのクライアントが切断されるまで、プロファイルは実際には消えません。 
  
 **DeleteProfile は** 、プロファイル内のすべてのメッセージ サービスのエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターを MSG_SERVICE_DELETE。 エントリ ポイント関数の呼び出しは、サービスがプロファイルから物理的に削除される前に行われます。 
  

