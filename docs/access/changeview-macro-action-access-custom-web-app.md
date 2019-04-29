---
title: changeview マクロアクション (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: ChangeView /ビューの変更アクションを使用して、ビュー間を移動できます。
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425359"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>changeview マクロアクション (Access カスタム web アプリ)

" **ChangeView** /ビューの変更" アクションを使用して、ビュー間を移動できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

"**ChangeView**/ビューの変更" アクションの引数は次のとおりです。 
  
|**アクションの引数**|**必須**|**説明**|
|:-----|:-----|:-----|
|Table  <br/> |はい  <br/> |開くテーブル名を指定します。  <br/> |
|View  <br/> |はい  <br/> |開くビューの名前を指定します。  <br/> |
|ここで  <br/> |いいえ  <br/> |指定した場合は、オブジェクト レコード ソースの Where 条件式を置換します。  <br/> |
|Order By  <br/> |いいえ  <br/> |レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。  <br/> |
   
## <a name="remarks"></a>注釈

ユーザーが適用したすべての並べ替えまたはフィルター処理は、" **ChangeView** /ビューの変更" アクションが呼び出されるとクリアされます。 
  
The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,). 
  
When you set the  *OrderBy*  argument, the records are sorted by default in ascending order. 
  

