---
title: GoToControl マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 6c286821-67d6-4d96-973a-bca7934c7672
description: GoToControl アクションを使用すると、開いているビューの現在のレコード内で指定したコントロールにフォーカスを移動できます。
ms.openlocfilehash: 5323f1daff2e8ae76c9aa24e6a40b907b6396030
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572474"
---
# <a name="gotocontrol-macro-action-access-custom-web-app"></a>GoToControl マクロ アクション (Access カスタム Web アプリ)

**GoToControl** アクションを使用すると、開いているビューの現在のレコード内で指定したコントロールにフォーカスを移動できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

**GoToControl** アクションの引数は次のとおりです。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
|**コントロール名** <br/> |フォーカスの移動先とするフィールドまたはコントロールの名前。これは、必須の引数です。  <br/> |
   
## <a name="remarks"></a>注釈

特定のフィールドまたはコントロールにフォーカスを移動する必要がある場合にこのアクションを使用できます。また、このアクションを使用して、特定の条件に従ってフォーム内をナビゲーションできます。たとえば、医療保険のフォームでユーザーが [既婚] コントロールに [いいえ] と入力した場合、[配偶者またはパートナーの名前] コントロールを自動的にスキップしてフォーカスを次のコントロールに移動できます。
  

