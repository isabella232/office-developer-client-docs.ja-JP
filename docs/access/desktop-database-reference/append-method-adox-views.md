---
title: Append メソッド (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477944"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="d3875-102">Append メソッド (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="d3875-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="d3875-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3875-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d3875-104">新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="d3875-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3875-105">構文</span><span class="sxs-lookup"><span data-stu-id="d3875-105">Syntax</span></span>

<span data-ttu-id="d3875-106">*ビュー*です。*名*、*コマンド*を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3875-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="d3875-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3875-107">Parameters</span></span>

  - <span data-ttu-id="d3875-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="d3875-108">*Name*</span></span>

  - <span data-ttu-id="d3875-109">作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3875-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="d3875-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="d3875-110">*Command*</span></span>

  - <span data-ttu-id="d3875-111">作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="d3875-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3875-112">解説</span><span class="sxs-lookup"><span data-stu-id="d3875-112">Remarks</span></span>

<span data-ttu-id="d3875-113">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3875-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="d3875-p101">ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="d3875-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="d3875-116">Microsoft Jet 用 OLE DB プロバイダーを使用して、 <STRONG>Views</STRONG>コレクションの<STRONG>Append</STRONG>メソッドができます<EM>コマンド</EM>パラメーターの<STRONG>表示</STRONG>ではなく、<STRONG>プロシージャ</STRONG>を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3875-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="d3875-117"><STRONG>Procedure</STRONG> がデータ ソースに追加され、 <STRONG>Views</STRONG> コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d3875-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="d3875-118"><STRONG>Append</STRONG> の後、 <STRONG>Procedures</STRONG> コレクションと <STRONG>Views</STRONG> コレクションが更新された場合、 <STRONG>Procedure</STRONG> は <STRONG>Views</STRONG> コレクション内に存在しなくなり、 <STRONG>Procedures</STRONG> コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3875-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>


