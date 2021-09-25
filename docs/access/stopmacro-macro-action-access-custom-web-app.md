---
title: StopMacro マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: StopMacro/マクロの中止アクションを使用すると、現在実行中のマクロを中止できます。
ms.openlocfilehash: 873937805bb96584dc08708cf2fe4eeadeec8b03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614732"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StopMacro マクロ アクション (Access カスタム Web アプリ)

" **StopMacro/マクロの中止** " アクションを使用すると、現在実行中のマクロを中止できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**StopMacro** アクションには引数はありません。 
  
## <a name="remarks"></a>注釈

通常、このアクションは、条件に応じてマクロを中止する必要がある場合に使用します。たとえば、現在のビューに入力された日付に受けた注文の合計を表示するビューを開くユーザー インターフェイス (UI) マクロを作成するとします。条件式を使用して、ダイアログ ボックスの [注文日] コントロールに入力された日付が有効であるかどうかを確認できます。有効でない場合は、 **MessageBox** アクションでエラー メッセージを表示し、 **StopMacro** アクションでこの UI マクロを中止できます。 
  

