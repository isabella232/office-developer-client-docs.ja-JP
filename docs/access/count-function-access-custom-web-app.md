---
title: Count 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: クエリまたはテーブルに含まれるレコードの数が返されます。
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798589"
---
# <a name="count-function-access-custom-web-app"></a>Count 関数 (カスタム web アプリケーションのアクセス)

クエリまたはテーブルに含まれるレコードの数が返されます。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**カウント**(*式*) 
  
**Count** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Expression*  <br/> |カウント、またはフィールドのデータを使用して計算を実行する式にするデータを含むフィールドを識別する文字列式です。 *式*のオペランドには、テーブルのフィールドまたは関数が (組み込みまたはユーザー定義することができますが、他の SQL ではない集計関数) の名前を含めることができます。 あらゆる種類のテキストを含む、データをカウントすることができます。  <br/> |
   
## <a name="remarks"></a>解説

Count 関数を使用すると、元になるクエリのレコード数をカウントできます。たとえば、Count 関数を使用して、特定の国または地域に出荷された注文の数をカウントできます。
  
**Count** (\*) では、グループ内の項目数が返されます。NULL 値および重複する値もカウントされます。 
  

