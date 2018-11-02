---
title: URL プロパティ (RDS のデスクトップのデータベース参照のアクセス)
TOCTitle: URL property (RDS)
ms:assetid: 722765dc-f89c-0131-73b1-69c56a795546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249457(v=office.15)
ms:contentKeyID: 48545603
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca1fdba5e5fd9b16b66fd71f2841890870de4d65
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925983"
---
# <a name="url-property-rds"></a><span data-ttu-id="c3f51-102">URL プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="c3f51-102">URL property (RDS)</span></span>


<span data-ttu-id="c3f51-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c3f51-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c3f51-104">相対 URL または絶対 URL を格納する文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="c3f51-104">Indicates a string that contains a relative or absolute URL.</span></span>

<span data-ttu-id="c3f51-105">**URL** プロパティは、デザイン時に [DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグで設定するか、実行時にスクリプト コードで設定できます。</span><span class="sxs-lookup"><span data-stu-id="c3f51-105">You can set the **URL** property at design time in the [DataControl](datacontrol-object-rds.md) object's OBJECT tag, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f51-106">構文</span><span class="sxs-lookup"><span data-stu-id="c3f51-106">Syntax</span></span>

<span data-ttu-id="c3f51-107">デザイン時:\<パラメーター名"URL"の値を = ="Server"\></span><span class="sxs-lookup"><span data-stu-id="c3f51-107">Design time: \<PARAM NAME="URL" VALUE="Server"\></span></span>

<span data-ttu-id="c3f51-108">実行時間: DataControl.URL="Server]</span><span class="sxs-lookup"><span data-stu-id="c3f51-108">Run time: DataControl.URL="Server"</span></span>

## <a name="parameters"></a><span data-ttu-id="c3f51-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c3f51-109">Parameters</span></span>

  - <span data-ttu-id="c3f51-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="c3f51-110">*Server*</span></span>

  - <span data-ttu-id="c3f51-111">有効な URL を格納する文字列型 ( **String** ) の値。</span><span class="sxs-lookup"><span data-stu-id="c3f51-111">A **String** value that contains a valid URL.</span></span>

  - <span data-ttu-id="c3f51-112">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c3f51-112">*DataControl*</span></span>

  - <span data-ttu-id="c3f51-113">**DataControl** オブジェクトを表すオブジェクト変数。</span><span class="sxs-lookup"><span data-stu-id="c3f51-113">An object variable that represents a **DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f51-114">解説</span><span class="sxs-lookup"><span data-stu-id="c3f51-114">Remarks</span></span>

<span data-ttu-id="c3f51-p101">通常、URL は、[Recordset](recordset-object-ado.md) を生成して返すことができる Active Server Page (.asp) ファイルを示します。したがって、サーバー側 **DataFactory** オブジェクトを呼び出したり、カスタム ビジネス オブジェクトをプログラムしたりしなくても、 [Recordset](datafactory-object-rdsserver.md) を取得できます。</span><span class="sxs-lookup"><span data-stu-id="c3f51-p101">Typically, the URL identifies an Active Server Page (.asp) file that can produce and return a [Recordset](recordset-object-ado.md). Therefore, the user can obtain a **Recordset** without having to invoke the server-side [DataFactory](datafactory-object-rdsserver.md) object, or program a custom business object.</span></span>

<span data-ttu-id="c3f51-117">**URL** プロパティが設定されている場合、 [SubmitChanges](submitchanges-method-rds.md) は URL で指定された場所に変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="c3f51-117">If the **URL** property has been set, [SubmitChanges](submitchanges-method-rds.md) will submit changes to the location specified by the URL.</span></span>

