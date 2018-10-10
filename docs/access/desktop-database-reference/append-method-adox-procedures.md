---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476563"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="caeeb-102">Append メソッド (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="caeeb-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="caeeb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="caeeb-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="caeeb-104">新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="caeeb-105">構文</span><span class="sxs-lookup"><span data-stu-id="caeeb-105">Syntax</span></span>

<span data-ttu-id="caeeb-106">*プロシージャ*です。*名*、*コマンド*を追加します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="caeeb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="caeeb-107">Parameters</span></span>

  - <span data-ttu-id="caeeb-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="caeeb-108">*Name*</span></span>

  - <span data-ttu-id="caeeb-109">新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="caeeb-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="caeeb-110">*Command*</span></span>

  - <span data-ttu-id="caeeb-111">新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="caeeb-112">解説</span><span class="sxs-lookup"><span data-stu-id="caeeb-112">Remarks</span></span>

<span data-ttu-id="caeeb-113">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="caeeb-p101">ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="caeeb-116">Microsoft Jet 用 OLE DB プロバイダーを使用して、<STRONG>プロシージャ</STRONG>コレクションの<STRONG>Append</STRONG>メソッドができます<EM>コマンド</EM>パラメーターの<STRONG>プロシージャ</STRONG>ではなく<STRONG>ビュー</STRONG>を指定します。</span><span class="sxs-lookup"><span data-stu-id="caeeb-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="caeeb-117"><STRONG>View</STRONG> がデータ ソースに追加され、 <STRONG>Procedures</STRONG> コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="caeeb-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="caeeb-118"><STRONG>Append</STRONG> の後、 <STRONG>Procedures</STRONG> コレクションと <STRONG>Views</STRONG> コレクションが更新された場合、 <STRONG>View</STRONG> は <STRONG>Procedures</STRONG> コレクション内に存在しなくなり、 <STRONG>Views</STRONG> コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="caeeb-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>


