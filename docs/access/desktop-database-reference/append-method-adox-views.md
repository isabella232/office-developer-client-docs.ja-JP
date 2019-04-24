---
title: Append メソッド (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297047"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="38e95-102">Append メソッド (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="38e95-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="38e95-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="38e95-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38e95-104">新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="38e95-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e95-105">構文</span><span class="sxs-lookup"><span data-stu-id="38e95-105">Syntax</span></span>

<span data-ttu-id="38e95-106">*ビュー*。Append*Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="38e95-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="38e95-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38e95-107">Parameters</span></span>

|<span data-ttu-id="38e95-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38e95-108">Parameter</span></span>|<span data-ttu-id="38e95-109">説明</span><span class="sxs-lookup"><span data-stu-id="38e95-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="38e95-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="38e95-110">*Name*</span></span> |<span data-ttu-id="38e95-111">作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="38e95-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="38e95-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="38e95-112">*Command*</span></span> |<span data-ttu-id="38e95-113">作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="38e95-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="38e95-114">注釈</span><span class="sxs-lookup"><span data-stu-id="38e95-114">Remarks</span></span>

<span data-ttu-id="38e95-115">**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="38e95-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="38e95-p101">ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。</span><span class="sxs-lookup"><span data-stu-id="38e95-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="38e95-p102">OLE DB Provider for Microsoft Jet を使用しているとき、**Views** コレクションの **Append** メソッドによって **View** ではなく **Procedure** を *Command* パラメーターに指定することができます。**Procedure** がデータ ソースに追加され、**Views** コレクションに追加されます。**Append** の後、**Procedures** コレクションと **Views** コレクションが更新された場合、**Procedure** は **Views** コレクション内に存在しなくなり、**Procedures** コレクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="38e95-p102">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter. The **Procedure** will be added to the data source and will be added to the **Views** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


