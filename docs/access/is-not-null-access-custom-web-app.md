---
title: IS [NOT] NULL (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: 指定した式が NULL かどうかを判断します。
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699318"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (Access カスタム Web アプリ)

指定した式が NULL かどうかを判断します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-JP/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 *expression* **IS** [  *NOT*  ] **NULL**
  
**IS [NOT] NULL** 述語には、次の引数が含まれています。 
  
|||
|:-----|:-----|
| *expression*  <br/> |任意の有効な式。  <br/> |
| *NOT*  <br/> |ブール値の結果を否定するように指定します。この述語は、戻り値を反転し、戻り値が NULL でない場合は TRUE が、NULL の場合は FALSE が返されます。  <br/> |
   
## <a name="remarks"></a>解説

*expression*  の値が NULL の場合、IS NULL では TRUE が返されます、それ以外の場合は FALSE が返されます。 
  
式の値が NULL の場合、IS NOT NULL では FALSE が返されます。それ以外の場合は TRUE が返されます。
  

