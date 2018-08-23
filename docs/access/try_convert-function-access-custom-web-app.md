---
title: Try_Convert 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: 指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798772"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Try_Convert 関数 (カスタム web アプリケーションのアクセス)

指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Try_Convert** (*DataType*, *Expression*) 
  
**Try_Convert** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DataType*  <br/> |*式*に変換するためにデータを入力します。  <br/> |
| *Expression*  <br/> |変換する値を指定します。  <br/> |
   
## <a name="remarks"></a>解説

 **Try_Convert** は渡された値を取得し、指定された  *DataType*  への変換を試みます。変換が成功した場合、 **Try_Convert** は  *DataType*  で指定された型で値を返します。エラーが発生した場合は null が返されます。ただし、明示的に許可されていない変換を要求すると、 **Try_Convert** はエラーになって失敗します。 
  

