---
title: Beep マクロアクション (Access デスクトップデータベースリファレンス)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296865"
---
# <a name="beep-macro-action"></a><span data-ttu-id="fd5f4-102">Beep マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="fd5f4-102">Beep macro action</span></span>


<span data-ttu-id="fd5f4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd5f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd5f4-104">"Beep/警告音" アクションを使用すると、スピーカーから警告音を鳴らすことができます。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="fd5f4-105">Setting</span><span class="sxs-lookup"><span data-stu-id="fd5f4-105">Setting</span></span>

<span data-ttu-id="fd5f4-106">"Beep/警告音" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd5f4-107">注釈</span><span class="sxs-lookup"><span data-stu-id="fd5f4-107">Remarks</span></span>

<span data-ttu-id="fd5f4-108">"Beep/警告音" アクションは、次のような場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="fd5f4-109">重要な画面変更があったとき。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="fd5f4-p101">不適切なデータがコントロールに入力されたとき。たとえば、テキスト ボックス コントロールに数値データが入力された場合などです。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-p101">The wrong kind of data has been entered in a control. For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="fd5f4-112">マクロが特定のポイントに達したときや、マクロのアクションが完了したとき。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="fd5f4-113">警告音の周波数と継続時間は、ハードウェアに依存するので、コンピューターの機種によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fd5f4-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="fd5f4-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span><span class="sxs-lookup"><span data-stu-id="fd5f4-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

