---
title: CloseDatabase マクロ アクション
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d55e2028027f0861b1e9ad00518d9c51180fdfc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919886"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="ae9ec-102">CloseDatabase マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ae9ec-102">CloseDatabase macro action</span></span>


<span data-ttu-id="ae9ec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae9ec-104">**CloseDatabase**アクションを使用すると、現在のデータベースを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="ae9ec-105">設定値</span><span class="sxs-lookup"><span data-stu-id="ae9ec-105">Setting</span></span>

<span data-ttu-id="ae9ec-106">**CloseDatabase**アクションの引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae9ec-107">解説</span><span class="sxs-lookup"><span data-stu-id="ae9ec-107">Remarks</span></span>

  - <span data-ttu-id="ae9ec-108">アクセスでは、次のマクロで**CloseDatabase**アクションのすべてのアクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="ae9ec-109">この操作には、として、[**ファイル**] タブをクリックし、**データベースを閉じる**をクリックし、同じ効果があります。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="ae9ec-110">未保存のオブジェクトは、開いている場合**CloseDatabase**アクションを実行すると、ダイアログ ボックスが表示、**データベースを閉じる**をクリックすると表示されるものと同じです。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="ae9ec-111">Visual Basic for Applications (VBA) モジュールで**CloseDatabase**アクションを実行するには、 **DoCmd**オブジェクトの**CloseDatabase**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae9ec-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

