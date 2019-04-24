---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297082"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="37552-102">Append メソッド (ADOX Procedures)</span><span class="sxs-lookup"><span data-stu-id="37552-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="37552-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="37552-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37552-104">新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="37552-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="37552-105">構文</span><span class="sxs-lookup"><span data-stu-id="37552-105">Syntax</span></span>

<span data-ttu-id="37552-106">*手順*。Append*Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="37552-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="37552-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37552-107">Parameters</span></span>

|<span data-ttu-id="37552-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37552-108">Parameter</span></span>|<span data-ttu-id="37552-109">説明</span><span class="sxs-lookup"><span data-stu-id="37552-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="37552-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="37552-110">*Name*</span></span> |<span data-ttu-id="37552-111">新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="37552-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="37552-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="37552-112">*Command*</span></span> |<span data-ttu-id="37552-113">新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="37552-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="37552-114">注釈</span><span class="sxs-lookup"><span data-stu-id="37552-114">Remarks</span></span>

<span data-ttu-id="37552-115">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。</span><span class="sxs-lookup"><span data-stu-id="37552-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="37552-p101">ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="37552-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="37552-p102">OLE DB Provider for Microsoft Jet を使用しているとき、**Procedures** コレクションの **Append** メソッドによって **Procedure** ではなく **View** を *Command* パラメーターに指定することができます。**View** がデータ ソースに追加され、**Procedures** コレクションに追加されます。**Append** の後、**Procedures** コレクションと **Views** コレクションが更新された場合、**View** は **Procedures** コレクション内に存在しなくなり、**Views** コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="37552-p102">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter. The **View** will be added to the data source and will be added to the **Procedures** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


