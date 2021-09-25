---
title: Sum 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: 式に含まれるすべての値の合計が返されます。
ms.openlocfilehash: 2e6b75d256776e9552939e124410d258be1c0d74
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605702"
---
# <a name="sum-function-access-custom-web-app"></a>Sum 関数 (Access カスタム Web アプリ)

式に含まれるすべての値の合計が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Sum** (*NumericExpression*) 
  
**Sum** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *NumericExpression*  <br/> |追加する数値データを含むフィールドを識別する式、またはそのフィールドのデータを使用して計算を実行する式。 *NumericExpression* のオペランドには、テーブル フィールド、定数、または関数の名前を含めできます (組み込み関数またはユーザー定義関数を使用できますが、他の SQL 集計関数のいずれかではありません)。  <br/> |
   
## <a name="remarks"></a>注釈

**Sum** 関数は、Null 値が含まれるレコードを無視します。 
  
**Sum** 関数は、数値列でのみ使用できます。 
  

