---
title: setlocalvar マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 12444313-1cfa-49ff-89da-3030fe75c13e
description: SetLocalVar/ローカル変数の設定アクションは、一時変数を作成し、それを特定の値に設定します。
ms.openlocfilehash: 2493bc5c908c551e171a8fa7d9eaeea699a04f72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310945"
---
# <a name="setlocalvar-macro-action-access-custom-web-app"></a>setlocalvar マクロアクション (Access カスタム web アプリ)

The **SetLocalVar** action creates a temporary variable and set it to a specific value. 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> "**SetLocalVar/ローカル変数の設定**" アクションは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

"SetLocalVar/ローカル変数の設定" アクションの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
|**名前** <br/> |はい  <br/> |変数の名前を指定する文字列。  <br/> |
|**Expression** <br/> |はい  <br/> |An expression that will be used to set the value for this temporary variable. Do not precede the expression with the equal sign (=). You can click the **Build** button to use the **Expression Builder** to set this argument.  <br/> |
   

