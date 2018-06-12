---
title: IIf 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: 条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798556"
---
# <a name="iif-function-access-custom-web-app"></a>IIf 関数 (カスタム web アプリケーションのアクセス)

条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**Iif 関数**(*条件*、 *TrueValue**偽となる値*) 
  
**IIf** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *条件*  <br/> |評価する式。  <br/> |
| *TrueValue*  <br/> |*条件*が True でかどうかに返す値または式です。  <br/> |
| *偽となる値*  <br/> |値または式は、*条件*が False を返します。  <br/> |
   
## <a name="example"></a>例

テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。 ミドル ネームのイニシャル] フィールドが空白の場合は、完全な名前を表示する] フィールドと [姓] フィールドのみが結合されます。
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


