---
title: Avg 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: 指定したフィールドにある値の集合の平均値を計算します。
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426724"
---
# <a name="avg-function-access-custom-web-app"></a>Avg 関数 (Access カスタム Web アプリ)

指定したフィールドにある値の集合の平均値を計算します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Avg** (*NumericExpression*) 
  
**Avg** 関数には、以下の引数があります。 
  
|**Arg1 と Arg2 の値**|**説明**|
|:-----|:-----|
|NumericExpression  <br/> |平均化する数値データを含むフィールド、またはそのフィールドのデータを使用して計算を実行する式を示す文字列式。 *NumericExpression* のオペランドには、テーブル フィールド、変数、または関数の名前を含めできます (組み込み関数またはユーザー定義の場合がありますが、他の SQL 集計関数のいずれかではありません)。  <br/> |
   
## <a name="remarks"></a>注釈

**Avg** 関数で計算される平均は、値の合計を値の個数で割った算術平均です。たとえば、平均運送料などを計算する場合に、 **Avg** 関数を使用します。 
  
**Avg** 関数は **Null** 値を除外して計算します。 
  

