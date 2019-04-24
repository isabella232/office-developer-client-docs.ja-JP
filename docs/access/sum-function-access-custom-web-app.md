---
title: Sum 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: 式に含まれるすべての値の合計が返されます。
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304236"
---
# <a name="sum-function-access-custom-web-app"></a>Sum 関数 (Access カスタム web アプリ)

式に含まれるすべての値の合計が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **合計**(*NumericExpression*) 
  
**Sum** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *NumericExpression*  <br/> |追加する数値データを含むフィールドを識別する式、またはそのフィールドのデータを使用して計算を実行する式を指定します。 *NumericExpression*のオペランドには、テーブルフィールドの名前、定数、または関数を含めることができます (組み込みまたはユーザー定義であっても、他の SQL 集計関数は使用できません)。  <br/> |
   
## <a name="remarks"></a>解説

**Sum** 関数は、Null 値が含まれるレコードを無視します。 
  
**Sum** 関数は、数値列でのみ使用できます。 
  

