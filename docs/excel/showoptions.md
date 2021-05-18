---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407698"
---
# <a name="showoptions"></a><span data-ttu-id="347af-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="347af-103">ShowOptions</span></span>

<span data-ttu-id="347af-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="347af-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="347af-p101">ユーザーから情報を収集するためのモーダル ダイアログ ボックスを表示します。このエントリ ポイントは、**[Excel のオプション]** ダイアログ ボックス (**[数式]** セクションの下にある **[詳細設定]** カテゴリ内) で、選択したクラスター コネクタの **[クラスターの種類]** ボックスの隣にある **[オプション]** ボタンをクリックすると呼び出されます。クラスター コネクタで、独自のオプション ダイアログのインターフェイスを実装するとともに、レジストリまたは他の場所に関連データを格納する必要があります。オプションは、クラスター コネクタ内部にあります。Excel には認識されません。</span><span class="sxs-lookup"><span data-stu-id="347af-p101">Shows a modal dialog box to collect information from the user. This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section). Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere. The options are internal to the cluster connector. Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="347af-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="347af-110">Parameters</span></span>

<span data-ttu-id="347af-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="347af-111">_hWndParent_</span></span>
  
> <span data-ttu-id="347af-112">Excel ウインドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="347af-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="347af-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="347af-113">Return value</span></span>

<span data-ttu-id="347af-114">ダイアログ ボックスが表示された場合は **xlHpcRetSuccess**、表示されなかった場合は **xlHpcRetCallFailed**。</span><span class="sxs-lookup"><span data-stu-id="347af-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="347af-115">注釈</span><span class="sxs-lookup"><span data-stu-id="347af-115">Remarks</span></span>

<span data-ttu-id="347af-116">クラスター コネクタでは、使用するクラスター サーバーなどの情報をユーザーから取得するために、このダイアログ ボックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="347af-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="347af-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="347af-117">See also</span></span>

- [<span data-ttu-id="347af-118">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="347af-118">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

