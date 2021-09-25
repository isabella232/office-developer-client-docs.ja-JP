---
title: ChangeView マクロ アクション (カスタム Web アプリへのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: ChangeView /ビューの変更アクションを使用して、ビュー間を移動できます。
ms.openlocfilehash: e1ff4487408deeafa56a9ca6bba9021c3c1f7769
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573342"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView マクロ アクション (カスタム Web アプリへのアクセス)

" **ChangeView** /ビューの変更" アクションを使用して、ビュー間を移動できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

"**ChangeView**/ビューの変更" アクションの引数は次のとおりです。 
  
|**アクションの引数**|**必須**|**説明**|
|:-----|:-----|:-----|
|Table  <br/> |必要  <br/> |開くテーブル名を指定します。  <br/> |
|表示  <br/> |必要  <br/> |開くビューの名前を指定します。  <br/> |
|場所  <br/> |いいえ  <br/> |指定した場合は、オブジェクト レコード ソースの Where 条件式を置換します。  <br/> |
|Order By  <br/> |いいえ  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

ユーザーが適用したすべての並べ替えまたはフィルター処理は、" **ChangeView** /ビューの変更" アクションが呼び出されるとクリアされます。 
  
The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). 
  
When you set the  *OrderBy*  argument, the records are sorted by default in ascending order. 
  

