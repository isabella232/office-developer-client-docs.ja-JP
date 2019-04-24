---
title: Var 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304201"
---
# <a name="var-function-access-custom-web-app"></a>Var 関数 (Access カスタム web アプリ)

クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Var**(*NumericExpression*) 
  
**Var** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *NumericExpression*  <br/> |評価する数値データを含むフィールドを識別するテキスト式。または、そのフィールドのデータを使用して計算を実行する式を指定します。 *NumericExpression*のオペランドには、テーブルフィールドの名前、定数、または関数を含めることができます (組み込みまたはユーザー定義であっても、他の SQL 集計関数は使用できません)。  <br/> |
   
## <a name="remarks"></a>解説

 **Var** は、数値列でのみ使用できます。Null 値は無視されます。 
  

