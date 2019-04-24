---
title: ADO 用の Visual C++ Extensions
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302755"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="fb6d5-102">ADO 用 Visual C++ Extensions</span><span class="sxs-lookup"><span data-stu-id="fb6d5-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="fb6d5-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb6d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb6d5-104">visual c++ で ado をプログラミングする方法として推奨されるのは、「 [Microsoft visual c++ ado プログラミング](visual-c-ado-programming.md)」で説明されているように、 \*\* \#import\*\*ディレクティブを使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="fb6d5-105">しかし、ADO の以前のバージョンでは、Visual C++ を使用するプログラミングの代替方法として、Visual C++ Extensions が提供されていました。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="fb6d5-106">このセクションでは、Visual C++ Extensions コードを維持する必要がある場合にこの機能について説明\#します。ただし、新しい ADO コードは**import**を使用して記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="fb6d5-p102">Visual C++ を使用するプログラマが、ADO でデータを取得する際に直面する手間のかかる作業の 1 つに、バリアント データ型 (Variant) として返されたデータを C++ データ型に変換し、変換したデータをさらにクラスまたは構造体に格納するという作業があります。バリアント データ型を使用して C++ データ型を取得すると、手間がかかるだけでなくパフォーマンスも低下します。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="fb6d5-p103">ADO には、バリアント型 (Variant) を使用しないでネイティブな C/C++ データ型のデータを取得できるインターフェイスと、そのインターフェイスを簡単に操作するためのプリプロセッサ マクロが用意されています。その結果、使用しやすく優れたパフォーマンスを持った、柔軟性のあるツールとなりました。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="fb6d5-p104">C/C++ クライアントでは、通常は、ネイティブ C/C++ 型を格納する C/C++ 構造体またはクラスに [Recordset](recordset-object-ado.md) のレコードをバインドします。バリアント型 (Variant) を使用する場合、バリアント型からネイティブ C/C++ 型に変換するコードを作成する必要があります。ADO 用の Visual C++ Extensions は、Visual C++ プログラマがこのような作業を簡単に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="fb6d5-114">ADO 用の Visual C++ Extensions の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb6d5-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="fb6d5-115">Visual C++ Extensions を使用する</span><span class="sxs-lookup"><span data-stu-id="fb6d5-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="fb6d5-116">Visual C++ Extensions のヘッダー</span><span class="sxs-lookup"><span data-stu-id="fb6d5-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="fb6d5-117">Visual C++ Extensions の例</span><span class="sxs-lookup"><span data-stu-id="fb6d5-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

