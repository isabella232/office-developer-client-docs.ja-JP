---
title: Append メソッド (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca51537c78dfc07a6cd3560bba7154f6b56ef31f
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861212"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="a81bc-102">Append メソッド (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="a81bc-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="a81bc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a81bc-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a81bc-104">新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81bc-105">構文</span><span class="sxs-lookup"><span data-stu-id="a81bc-105">Syntax</span></span>

<span data-ttu-id="a81bc-106">*ビュー*です。*名*、*コマンド*を追加します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="a81bc-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a81bc-107">Parameters</span></span>

  - <span data-ttu-id="a81bc-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="a81bc-108">*Name*</span></span>

  - <span data-ttu-id="a81bc-109">作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="a81bc-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="a81bc-110">*Command*</span></span>

  - <span data-ttu-id="a81bc-111">作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="a81bc-112">解説</span><span class="sxs-lookup"><span data-stu-id="a81bc-112">Remarks</span></span>

<span data-ttu-id="a81bc-113">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="a81bc-p101">ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="a81bc-116">Microsoft Jet 用 OLE DB プロバイダーを使用して、 **Views**コレクションの**Append**メソッドができます*コマンド*パラメーターの**表示**ではなく、**プロシージャ**を指定します。</span><span class="sxs-lookup"><span data-stu-id="a81bc-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="a81bc-117">**Procedure** がデータ ソースに追加され、 **Views** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="a81bc-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="a81bc-118">**Append** の後、 **Procedures** コレクションと **Views** コレクションが更新された場合、 **Procedure** は **Views** コレクション内に存在しなくなり、 **Procedures** コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a81bc-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


