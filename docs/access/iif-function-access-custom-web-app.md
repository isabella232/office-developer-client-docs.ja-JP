---
title: IIf 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: 条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301863"
---
# <a name="iif-function-access-custom-web-app"></a>IIf 関数 (Access カスタム web アプリ)

条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**IIf**(*Condition*、 *TrueValue*、 *false 値*) 
  
**IIf** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Condition*  <br/> |評価する式。  <br/> |
| *TrueValue*  <br/> |*Condition*が True の場合に返される値または式。  <br/> |
| *false 値*  <br/> |*Condition*が False の場合に返される値または式。  <br/> |
   
## <a name="example"></a>例

テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。 MiddleInitial フィールドが空白の場合は、姓と名のフィールドだけが組み合わせられ、氏名が表示されます。
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


