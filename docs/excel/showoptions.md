---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798945"
---
# <a name="showoptions"></a><span data-ttu-id="0609d-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="0609d-103">ShowOptions</span></span>

<span data-ttu-id="0609d-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0609d-104">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0609d-105">ユーザーから情報を収集するためのモーダル ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="0609d-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="0609d-106">このエントリ ポイントは、**[Excel のオプション]** ダイアログ ボックス (**[数式]** セクションの下にある **[詳細設定]** カテゴリ内) で、選択したクラスター コネクタの **[クラスターの種類]** ボックスの隣にある **[オプション]** ボタンをクリックすると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0609d-106">Shows a modal dialog box to collect information from the user. This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section). Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere. The options are internal to the cluster connector. Excel is not aware of them.</span></span> <span data-ttu-id="0609d-107">クラスター コネクタで、独自のオプション ダイアログのインターフェイスを実装するとともに、レジストリまたは他の場所に関連データを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0609d-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="0609d-108">オプションは、クラスター コネクタ内部にあります。</span><span class="sxs-lookup"><span data-stu-id="0609d-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="0609d-109">Excel には認識されません。</span><span class="sxs-lookup"><span data-stu-id="0609d-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="0609d-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0609d-110">Parameters</span></span>

<span data-ttu-id="0609d-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="0609d-111">_hWndParent_</span></span>
  
> <span data-ttu-id="0609d-112">Excel ウインドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0609d-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0609d-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="0609d-113">Return value</span></span>

<span data-ttu-id="0609d-114">ダイアログ ボックスが表示された場合は **xlHpcRetSuccess**、表示されなかった場合は **xlHpcRetCallFailed**。</span><span class="sxs-lookup"><span data-stu-id="0609d-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0609d-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0609d-115">Remarks</span></span>

<span data-ttu-id="0609d-116">クラスター コネクタでは、使用するクラスター サーバーなどの情報をユーザーから取得するために、このダイアログ ボックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0609d-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0609d-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="0609d-117">See also</span></span>

- [<span data-ttu-id="0609d-118">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="0609d-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

