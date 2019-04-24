---
title: QueryDef プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d826781bd668cff0a61c655e55834512a289c17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301093"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="5bc50-102">QueryDef プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="5bc50-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="5bc50-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5bc50-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5bc50-104">ローカルにキャッシュされる ODBC データソースから取得したレコード数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="5bc50-104">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="5bc50-105">値の取得と設定が可能な長整数型 (**Long**) の値です。</span><span class="sxs-lookup"><span data-stu-id="5bc50-105">Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc50-106">構文</span><span class="sxs-lookup"><span data-stu-id="5bc50-106">Syntax</span></span>

<span data-ttu-id="5bc50-107">*式*。CacheSize</span><span class="sxs-lookup"><span data-stu-id="5bc50-107">*expression* .CacheSize</span></span>

<span data-ttu-id="5bc50-108">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5bc50-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bc50-109">注釈</span><span class="sxs-lookup"><span data-stu-id="5bc50-109">Remarks</span></span>

<span data-ttu-id="5bc50-p102">**CacheSize** プロパティの値は、5 ～ 1200 の範囲で、利用可能な空きメモリが許容できる値より大きくならないように設定する必要があります。通常の値は 100 です。0 に設定すると、キャッシュがオフになります。</span><span class="sxs-lookup"><span data-stu-id="5bc50-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="5bc50-113">Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。</span><span class="sxs-lookup"><span data-stu-id="5bc50-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="5bc50-114">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="5bc50-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

