---
title: 重要で役に立つ C API XLM 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434516"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a>重要で役に立つ C API XLM 関数

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
このセクションで説明する関数は、DLL や XLL 開発者に特に便利な Microsoft Excel のコールバック関数です。これらの関数のうち、**xlfRegister** は、XLL と DLL で関数とコマンドを登録して Excel から直接呼び出せるようにする場合、必要不可欠です。DLL と XLL の関数やコマンドを登録解除するには、**xlfUnregister** 関数と **xlfSetName** 関数を組み合わせて使用します。 
  
多くの関数は、XLL の開発時の役立つ C API を通じて、Excel によって公開されます。これらは Excel ワークシートに対応する関数と、XLM マクロ シートで使用できる関数およびコマンドです。
  
## <a name="in-this-section"></a>このセクションの内容

[xlfCaller](xlfcaller.md)
  
[xlfEvaluate](xlfevaluate.md)
  
[xlfGetDef](xlfgetdef.md)
  
[xlfGetName](xlfgetname.md)
  
[xlfRegister (形式 1)](xlfregister-form-1.md)
  
[xlfRegister (形式 2)](xlfregister-form-2.md)
  
[xlfRegisterId](xlfregisterid.md)
  
[xlfUnregister (形式 1)](xlfunregister-form-1.md)
  
[xlfUnregister (形式 2)](xlfunregister-form-2.md)
  
[xlfSetName](xlfsetname.md)
  

