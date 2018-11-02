---
title: Append メソッド (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ccba425e74321f4ab760e9ddc4a722295290ffd1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925157"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="371a8-102">Append メソッド (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="371a8-102">Append method (ADOX Views)</span></span>


<span data-ttu-id="371a8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="371a8-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="371a8-104">新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="371a8-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="371a8-105">構文</span><span class="sxs-lookup"><span data-stu-id="371a8-105">Syntax</span></span>

<span data-ttu-id="371a8-106">*ビュー*です。*名*、*コマンド*を追加します。</span><span class="sxs-lookup"><span data-stu-id="371a8-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="371a8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="371a8-107">Parameters</span></span>

  - <span data-ttu-id="371a8-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="371a8-108">*Name*</span></span>

  - <span data-ttu-id="371a8-109">作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="371a8-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="371a8-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="371a8-110">*Command*</span></span>

  - <span data-ttu-id="371a8-111">作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="371a8-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="371a8-112">解説</span><span class="sxs-lookup"><span data-stu-id="371a8-112">Remarks</span></span>

<span data-ttu-id="371a8-113">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="371a8-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="371a8-p101">ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="371a8-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="371a8-116">Microsoft Jet 用 OLE DB プロバイダーを使用して、 **Views**コレクションの**Append**メソッドができます*コマンド*パラメーターの**表示**ではなく、**プロシージャ**を指定します。</span><span class="sxs-lookup"><span data-stu-id="371a8-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="371a8-117">**Procedure** がデータ ソースに追加され、 **Views** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="371a8-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="371a8-118">**Append** の後、 **Procedures** コレクションと **Views** コレクションが更新された場合、 **Procedure** は **Views** コレクション内に存在しなくなり、 **Procedures** コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="371a8-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


