---
title: Try_Convert 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: 指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410897"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Try_Convert 関数 (Access カスタム web アプリ)

指定したデータ型に値を変換します。変換が無効な場合は Null を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Try_Convert** (*DataType*, *Expression*) 
  
**Try_Convert** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *DataType*  <br/> |変換する*式*のデータ型を指定します。  <br/> |
| *Expression*  <br/> |変換する値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

 **Try_Convert** は渡された値を取得し、指定された  *DataType*  への変換を試みます。変換が成功した場合、 **Try_Convert** は  *DataType*  で指定された型で値を返します。エラーが発生した場合は null が返されます。ただし、明示的に許可されていない変換を要求すると、 **Try_Convert** はエラーになって失敗します。 
  

