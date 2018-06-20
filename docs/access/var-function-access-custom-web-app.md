---
title: Var 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798762"
---
# <a name="var-function-access-custom-web-app"></a>Var 関数 (カスタム web アプリケーションのアクセス)

クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Var**(*数式*) 
  
**Var** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *数式*  <br/> |評価する数値データ、またはそのフィールドのデータを使用して計算を実行する式を含むフィールドを識別する文字列式です。 *数式*内のオペランドには、テーブルのフィールド、定数、または関数 (組み込みまたはユーザー定義することができますが、他の SQL 集計関数のいずれかのない) の名前を含めることができます。  <br/> |
   
## <a name="remarks"></a>解説

 **Var** は、数値列でのみ使用できます。Null 値は無視されます。 
  

