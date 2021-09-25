---
title: Var 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
ms.openlocfilehash: a6ce06ea74c32a52685d1debee14345b193920e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588393"
---
# <a name="var-function-access-custom-web-app"></a>Var 関数 (Access カスタム Web アプリ)

クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Var** (*NumericExpression*) 
  
**Var** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *NumericExpression*  <br/> |評価する数値データを含むフィールド、またはそのフィールドのデータを使用して計算を実行する式を示すテキスト式。 *NumericExpression* のオペランドには、テーブル フィールド、定数、または関数の名前を含めできます (組み込み関数またはユーザー定義関数を使用できますが、他の SQL 集計関数のいずれかではありません)。  <br/> |
   
## <a name="remarks"></a>注釈

 **Var** は、数値列でのみ使用できます。Null 値は無視されます。 
  

