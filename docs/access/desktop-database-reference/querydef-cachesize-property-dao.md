---
title: QueryDef.CacheSize プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: a84d990e-8180-daa3-7640-47d2be8fd28b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821397(v=office.15)
ms:contentKeyID: 48546899
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9d22b35e63d9ad3a92d0f73a2ddaa98661de6a6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926032"
---
# <a name="querydefcachesize-property-dao"></a><span data-ttu-id="e2c77-102">QueryDef.CacheSize プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e2c77-102">QueryDef.CacheSize property (DAO)</span></span>


<span data-ttu-id="e2c77-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e2c77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2c77-p101">ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2c77-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c77-106">構文</span><span class="sxs-lookup"><span data-stu-id="e2c77-106">Syntax</span></span>

<span data-ttu-id="e2c77-107">*式*です。CacheSize</span><span class="sxs-lookup"><span data-stu-id="e2c77-107">*expression* .CacheSize</span></span>

<span data-ttu-id="e2c77-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e2c77-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c77-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e2c77-109">Remarks</span></span>

<span data-ttu-id="e2c77-p102">**CacheSize** プロパティの値は、5 ～ 1200 の範囲で、利用可能な空きメモリが許容できる値より大きくならないように設定する必要があります。通常の値は 100 です。0 に設定すると、キャッシュがオフになります。</span><span class="sxs-lookup"><span data-stu-id="e2c77-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="e2c77-113">Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。</span><span class="sxs-lookup"><span data-stu-id="e2c77-113">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="e2c77-114">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="e2c77-114">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

