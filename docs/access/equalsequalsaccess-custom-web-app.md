---
title: Equals (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: 2 つの値が等しいかどうかを比較します。
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408930"
---
# <a name="equals-access-custom-web-app"></a>Equals (Access カスタム web アプリ)

2 つの値が等しいかどうかを比較します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

`= (Equals)`

*expression*  =  *expression* 
  
*expression*  は任意の有効な式です。これらの式のデータ型が異なる場合、一方のデータ型に、もう一方のデータ型に暗黙的に変換可能なデータ型を使用する必要があります。変換はデータ型の優先順位の規則によって決まります。 
  
## <a name="return-type"></a>戻り値の型

**Boolean**
  
## <a name="remarks"></a>注釈

2 つの NULL 式を比較した場合、結果は TRUE になります。
  
NULL 値を NULL 以外の値と比較した場合、結果は常に FALSE になります。
  

