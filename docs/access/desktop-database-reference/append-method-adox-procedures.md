---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195cb08fb0b195b63cdddaa848554f24d028b498
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861877"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="2dce7-102">Append メソッド (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="2dce7-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="2dce7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dce7-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2dce7-104">新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dce7-105">構文</span><span class="sxs-lookup"><span data-stu-id="2dce7-105">Syntax</span></span>

<span data-ttu-id="2dce7-106">*プロシージャ*です。*名*、*コマンド*を追加します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="2dce7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2dce7-107">Parameters</span></span>

  - <span data-ttu-id="2dce7-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="2dce7-108">*Name*</span></span>

  - <span data-ttu-id="2dce7-109">新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="2dce7-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="2dce7-110">*Command*</span></span>

  - <span data-ttu-id="2dce7-111">新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dce7-112">解説</span><span class="sxs-lookup"><span data-stu-id="2dce7-112">Remarks</span></span>

<span data-ttu-id="2dce7-113">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="2dce7-p101">ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="2dce7-116">Microsoft Jet 用 OLE DB プロバイダーを使用して、**プロシージャ**コレクションの**Append**メソッドができます*コマンド*パラメーターの**プロシージャ**ではなく**ビュー**を指定します。</span><span class="sxs-lookup"><span data-stu-id="2dce7-116">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="2dce7-117">**View** がデータ ソースに追加され、 **Procedures** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="2dce7-117">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="2dce7-118">**Append** の後、 **Procedures** コレクションと **Views** コレクションが更新された場合、 **View** は **Procedures** コレクション内に存在しなくなり、 **Views** コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2dce7-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


