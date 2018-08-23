---
title: ChangeView マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: ChangeView /ビューの変更アクションを使用して、ビュー間を移動できます。
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798585"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView マクロのアクション (カスタム web アプリケーションのアクセス)

" **ChangeView** /ビューの変更" アクションを使用して、ビュー間を移動できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

" **ChangeView** /ビューの変更" アクションの引数は次のとおりです。 
  
|**アクションの引数**|**必須**|**説明**|
|:-----|:-----|:-----|
|Table  <br/> |はい  <br/> |開くテーブル名を指定します。  <br/> |
|View  <br/> |はい  <br/> |開くビューの名前を指定します。  <br/> |
|Where  <br/> |いいえ  <br/> |指定した場合は、オブジェクト レコード ソースの Where 条件式を置換します。  <br/> |
|Order By  <br/> |いいえ  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

ユーザーが適用したすべての並べ替えまたはフィルター処理は、" **ChangeView** /ビューの変更" アクションが呼び出されるとクリアされます。 
  
*並べ替え*引数は、フィールドまたはレコードをソートするフィールドの名前です。 複数のフィールド名を指定する場合はコンマ (,) で区切ります。 
  
*並べ替え*引数を設定すると、既定では昇順でレコードが並べ替えられます。 
  

