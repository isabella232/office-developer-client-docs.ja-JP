---
title: '[しない] が NULL (カスタム web アプリケーションのアクセス)'
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: 指定した式が NULL かどうかを判別します。
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798583"
---
# <a name="is-not-null-access-custom-web-app"></a>[しない] が NULL (カスタム web アプリケーションのアクセス)

指定した式が NULL かどうかを判別します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *expression* **IS** [  *NOT*  ] **NULL**
  
**IS [NOT] NULL** 述語には次の引数があります。 
  
|||
|:-----|:-----|
| *expression*  <br/> |任意の有効な式。  <br/> |
| *NOT*  <br/> |ブール値の結果を否定するように指定します。この述語は、戻り値を反転し、戻り値が NULL でない場合は TRUE が、NULL の場合は FALSE が返されます。  <br/> |
   
## <a name="remarks"></a>解説

*expression*  の値が NULL の場合、IS NULL では TRUE が返されます、それ以外の場合は FALSE が返されます。 
  
式の値が NULL の場合、IS NOT NULL では FALSE が返されます。それ以外の場合は TRUE が返されます。
  

