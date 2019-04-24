---
title: Count 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: クエリまたはテーブルに含まれるレコードの数が返されます。
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282237"
---
# <a name="count-function-access-custom-web-app"></a>Count 関数 (Access カスタム web アプリ)

クエリまたはテーブルに含まれるレコードの数が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**Count**(*式*) 
  
**Count** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Expression*  <br/> |計算するデータを含むフィールドを識別する文字列式、またはフィールドのデータを使用して計算を実行する式を指定します。 *Expression*のオペランドには、テーブルのフィールドまたは関数の名前を含めることができます (組み込みまたはユーザー定義であっても、他の SQL 集計関数は使用できません)。 テキストを含む任意の種類のデータをカウントできます。  <br/> |
   
## <a name="remarks"></a>解説

Count 関数を使用すると、元になるクエリのレコード数をカウントできます。たとえば、Count 関数を使用して、特定の国または地域に出荷された注文の数をカウントできます。
  
**Count** (\*) では、グループ内の項目数が返されます。NULL 値および重複する値もカウントされます。 
  

