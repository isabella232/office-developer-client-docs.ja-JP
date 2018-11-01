---
title: ADO 用の Visual C++ Extensions
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4e0d9e9f5db8741cb04fd4d576ea67408285aac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881763"
---
# <a name="visual-c-extensions-for-ado"></a><span data-ttu-id="91179-102">ADO 用の Visual C++ Extensions</span><span class="sxs-lookup"><span data-stu-id="91179-102">Visual C++ Extensions for ADO</span></span>


<span data-ttu-id="91179-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="91179-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91179-104">ADO Visual C++ でのプログラミングの推奨される方法を使用して、**\#インポート**ディレクティブについては、 [Microsoft Visual C++ での ADO プログラミング](visual-c-ado-programming.md)で説明したようです。</span><span class="sxs-lookup"><span data-stu-id="91179-104">The preferred method of programming ADO with Visual C++ is using the **\#import** directive, as discussed in [Microsoft Visual C++ ADO Programming](visual-c-ado-programming.md).</span></span> <span data-ttu-id="91179-105">しかし、ADO の以前のバージョンでは、Visual C++ を使用するプログラミングの代替方法として、Visual C++ Extensions が提供されていました。</span><span class="sxs-lookup"><span data-stu-id="91179-105">However, earlier versions of ADO shipped with an alternate method of programming using Visual C++: the Visual C++ Extensions.</span></span> <span data-ttu-id="91179-106">ここで Visual C++ の拡張機能のコードを維持する必要があります人のためのこの機能の説明ですが、使用して新しい ADO コードを記述する必要があります\#**をインポート**します。</span><span class="sxs-lookup"><span data-stu-id="91179-106">This section documents this feature for those who must maintain Visual C++ Extensions code, but new ADO code should be written using \#**import**.</span></span>

<span data-ttu-id="91179-p102">Visual C++ を使用するプログラマが、ADO でデータを取得する際に直面する手間のかかる作業の 1 つに、バリアント データ型 (Variant) として返されたデータを C++ データ型に変換し、変換したデータをさらにクラスまたは構造体に格納するという作業があります。バリアント データ型を使用して C++ データ型を取得すると、手間がかかるだけでなくパフォーマンスも低下します。</span><span class="sxs-lookup"><span data-stu-id="91179-p102">One of the most tedious jobs Visual C++ programmers face when retrieving data with ADO is converting data returned as a VARIANT data type into a C++ data type, and then storing the converted data in a class or structure. In addition to being cumbersome, retrieving C++ data through a VARIANT data type diminishes performance.</span></span>

<span data-ttu-id="91179-p103">ADO には、バリアント型 (Variant) を使用しないでネイティブな C/C++ データ型のデータを取得できるインターフェイスと、そのインターフェイスを簡単に操作するためのプリプロセッサ マクロが用意されています。その結果、使用しやすく優れたパフォーマンスを持った、柔軟性のあるツールとなりました。</span><span class="sxs-lookup"><span data-stu-id="91179-p103">ADO provides an interface that supports retrieving data into native C/C++ data types without going through a VARIANT, and also provides preprocessor macros that simplify using the interface. The result is a flexible tool that is easier to use and has great performance.</span></span>

<span data-ttu-id="91179-p104">C/C++ クライアントでは、通常は、ネイティブ C/C++ 型を格納する C/C++ 構造体またはクラスに [Recordset](recordset-object-ado.md) のレコードをバインドします。バリアント型 (Variant) を使用する場合、バリアント型からネイティブ C/C++ 型に変換するコードを作成する必要があります。ADO 用の Visual C++ Extensions は、Visual C++ プログラマがこのような作業を簡単に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="91179-p104">A common C/C++ client scenario is to bind a record in a [Recordset](recordset-object-ado.md) to a C/C++ struct or class containing native C/C++ types. When going through VARIANTs, this involves writing conversion code from VARIANT to C/C++ native types. The Visual C++ Extensions for ADO are targeted at making this scenario much easier for the Visual C++ programmer.</span></span>

<span data-ttu-id="91179-114">ADO 用の Visual C++ Extensions の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="91179-114">See the following topics to learn more about the Visual C++ Extensions for ADO.</span></span>

  - [<span data-ttu-id="91179-115">Visual C++ Extensions を使用する</span><span class="sxs-lookup"><span data-stu-id="91179-115">Using Visual C++ Extensions for ADO</span></span>](using-visual-c-extensions.md)

  - [<span data-ttu-id="91179-116">Visual C++ Extensions のヘッダー</span><span class="sxs-lookup"><span data-stu-id="91179-116">Visual C++ Extensions Header</span></span>](visual-c-extensions-header.md)

  - [<span data-ttu-id="91179-117">Visual C++ Extensions の例</span><span class="sxs-lookup"><span data-stu-id="91179-117">ADO with Visual C++ Extensions Example</span></span>](visual-c-extensions-example.md)

