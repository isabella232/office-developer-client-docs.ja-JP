---
title: '15 章:  ADOX に関する基本事項'
TOCTitle: 'Chapter 15: ADOX Fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3869f23b93df78fd207812a85f91dd3272bd255f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479267"
---
# <a name="chapter-15-adox-fundamentals"></a><span data-ttu-id="64be9-102">15 章: ADOX に関する基本事項</span><span class="sxs-lookup"><span data-stu-id="64be9-102">Chapter 15: ADOX Fundamentals</span></span>


<span data-ttu-id="64be9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="64be9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="64be9-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) は、ADO オブジェクトおよびプログラミング モデルの拡張機能です。ADOX には、セキュリティに加え、スキーマの作成および変更のためのオブジェクトが含まれます。オブジェクト ベースでスキーマ操作が行われるため、さまざまなデータ ソースに対してそれぞれの文法の違いに関係なく動作するコードを記述することができます。</span><span class="sxs-lookup"><span data-stu-id="64be9-p101">Microsoft® ActiveX® Data Objects Extensions for Data Definition Language and Security (ADOX) is an extension to the ADO objects and programming model. ADOX includes objects for schema creation and modification, as well as security. Because it is an object-based approach to schema manipulation, you can write code that will work against various data sources regardless of differences in their native syntaxes.</span></span>

<span data-ttu-id="64be9-p102">ADOX は、コア ADO オブジェクトに付随するライブラリです。これにより、テーブルやプロシージャなどのスキーマ オブジェクトの作成、修正、および削除のための追加オブジェクトが提供されます。これにはまた、ユーザーおよびグループを管理し、オブジェクトに対する権限を与えたり取り消すためのセキュリティ オブジェクトも含まれます。</span><span class="sxs-lookup"><span data-stu-id="64be9-p102">ADOX is a companion library to the core ADO objects. It exposes additional objects for creating, modifying, and deleting schema objects, such as tables and procedures. It also includes security objects to maintain users and groups and to grant and revoke permissions on objects.</span></span>

<span data-ttu-id="64be9-p103">開発ツールで ADOX を使用するには、ADOX タイプ ライブラリへの参照を確立する必要があります。ADOX ライブラリとは、Microsoft ADO Ext. for DDL and Security のことです。ADOX ライブラリのファイル名は Msadox.dll で、プログラム ID (ProgID) は "ADOX" です。ライブラリへの参照を確立する方法の詳細については、開発ツールのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64be9-p103">To use ADOX with your development tool, you should establish a reference to the ADOX type library. The description of the ADOX library is "Microsoft ADO Ext. for DDL and Security." The ADOX library file name is Msadox.dll, and the program ID (ProgID) is "ADOX". For more information about establishing references to libraries, see the documentation of your development tool.</span></span>

<span data-ttu-id="64be9-p104">Microsoft OLE DB Provider for the Microsoft Jet Database Engine は、ADOX を完全にサポートしています。データ プロバイダーによっては、ADOX の特定の機能がサポートされていない場合があります。Microsoft OLE DB Provider for ODBC、Microsoft OLE DB Provider for Oracle、または Microsoft SQL Server OLE DB Provider でサポートされている機能に関する詳細については、MDAC の Readme ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64be9-p104">The Microsoft OLE DB Provider for the Microsoft Jet Database Engine fully supports ADOX. Certain features of ADOX may not be supported, depending on your data provider. For more information about supported features with the Microsoft OLE DB Provider for ODBC, the Microsoft OLE DB Provider for Oracle, or the Microsoft SQL Server OLE DB Provider, see the MDAC readme file.</span></span>

<span data-ttu-id="64be9-p105">このドキュメントは、Microsoft® Visual Basic® のプログラミング言語を使用できる知識および ADO に関する一般的な知識を持っていることを前提としています。ADO の詳細については、「[ADO プログラマ ガイド](ado-programmer-s-guide.md)」を参照してください。ADOX に関する概要については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64be9-p105">This document assumes a working knowledge of the Microsoft® Visual Basic® programming language and a general knowledge of ADO. For more information about ADO, see the [ADO Programmer's Guide](ado-programmer-s-guide.md). For more overview information about ADOX, see the following topics:</span></span>

  - [<span data-ttu-id="64be9-120">ADOX オブジェクト</span><span class="sxs-lookup"><span data-stu-id="64be9-120">ADOX Objects</span></span>](adox-objects.md)

  - [<span data-ttu-id="64be9-121">ADOX コレクション</span><span class="sxs-lookup"><span data-stu-id="64be9-121">ADOX Collections</span></span>](adox-collections.md)

  - [<span data-ttu-id="64be9-122">ADOX のプロパティ</span><span class="sxs-lookup"><span data-stu-id="64be9-122">ADOX Properties</span></span>](adox-properties.md)

  - [<span data-ttu-id="64be9-123">ADOX メソッド</span><span class="sxs-lookup"><span data-stu-id="64be9-123">ADOX Methods</span></span>](adox-methods.md)

  - [<span data-ttu-id="64be9-124">ADOX コードの例</span><span class="sxs-lookup"><span data-stu-id="64be9-124">ADOX Examples</span></span>](adox-code-examples.md)
