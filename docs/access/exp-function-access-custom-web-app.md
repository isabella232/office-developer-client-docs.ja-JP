---
title: Exp 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: 指定した式の指数値を戻します。
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798558"
---
# <a name="exp-function-access-custom-web-app"></a>Exp 関数 (カスタム web アプリケーションのアクセス)

指定した式の指数値を戻します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Exp**(*数式*) 
  
**Exp** 関数には以下の引数が含まれます。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *数式*  <br/> |Double 型、または Double に暗黙的に変換できる式。  <br/> |
   
## <a name="remarks"></a>注釈

定数 **e** (2.718281...) は、自然対数の基数です。 
  
ある数値の指数とは、定数 **e** をべき乗する数値です。たとえば、 **Exp** (1.0) = e^1.0 = 2.71828182845905 となり、 **Exp** (10) = e^10 = 22026.4657948067 となります。 
  
数値の自然対数の指数は、番号自体: **Exp** (LOG (n)) = n です。 数値の指数の自然対数は、番号自体: ログ (**Exp** (n)) = n です。 
  

