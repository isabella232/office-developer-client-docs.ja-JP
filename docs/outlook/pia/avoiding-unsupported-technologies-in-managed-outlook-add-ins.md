---
title: マネージ Outlook アドインでサポートされないテクノロジを回避する
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359060"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a><span data-ttu-id="4471c-102">マネージ Outlook アドインでサポートされないテクノロジを回避する</span><span class="sxs-lookup"><span data-stu-id="4471c-102">Avoiding unsupported technologies in managed Outlook add-ins</span></span>

<span data-ttu-id="4471c-103">.NET Framework よりも前からあるテクノロジの一部は、マネージ コード プログラミングではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4471c-103">Certain technologies that predate the .NET Framework are not supported in managed code programming.</span></span> <span data-ttu-id="4471c-104">それらのテクノロジには、コラボレーション データ オブジェクト (CDO)、Messaging Application Programming Interface (MAPI、または Extended MAPI とも呼ばれる)、Simple MAPI などがあります。</span><span class="sxs-lookup"><span data-stu-id="4471c-104">These technologies include Collaboration Data Objects (CDO), Messaging Application Programming Interface (MAPI, often known as Extended MAPI), and Simple MAPI.</span></span> <span data-ttu-id="4471c-105">これらのテクノロジの設計と開発にはアンマネージ コードが使われており、Microsoft は、それらをマネージ アプリケーションで使用するための正式のマネージ ラッパーを提供していません。</span><span class="sxs-lookup"><span data-stu-id="4471c-105">These technologies were designed and developed with unmanaged code, and Microsoft does not provide official managed wrappers to support their use in managed applications.</span></span> 

<span data-ttu-id="4471c-106">詳細については、「[文書番号 266353: クライアント側のメッセージングの開発のサポート ガイドライン](https://go.microsoft.com/fwlink/?linkid=89209)」のセクション「マネージ コードでサポートされている API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4471c-106">For more information, see the section "APIs that are supported in managed code" in the article [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span></span>

<span data-ttu-id="4471c-107">ただし、Microsoft Outlook には、以前は CDO や Exchange クライアント拡張機能 (ECE) でしか解決できなかった問題を処理する多くのオブジェクト モデルが開発者向けに用意されています。</span><span class="sxs-lookup"><span data-stu-id="4471c-107">Nonetheless, Microsoft Outlook offers many object model features that achieve what previously only CDO and Exchange Client Extensions (ECE) solved for developers.</span></span> <span data-ttu-id="4471c-108">Outlook の既存のアンマネージ アプリケーションで CDO を使用していて、マネージ ソリューションに CDO のサポートがないためにアプリケーションをマネージ コードに移行できない場合は、Outlook オブジェクト モデルとプライマリ相互運用機能アセンブリ (PIA) だけを使用して CDO に頼らなくて済むようにソリューションを更新することで、マネージ コードにすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="4471c-108">If you use CDO in an existing unmanaged Outlook application and the lack of support for CDO in managed solutions has hindered you from migrating the application to managed code, you can now consider updating your solution to managed code, using only the Outlook object model and the Primary Interop Assembly (PIA), without having to resort to CDO.</span></span> 

<span data-ttu-id="4471c-109">Outlook 2007 で CDO および ECE への依存度を下げるために導入された、より総合的な Outlook プラットフォームの詳細については、「[What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\))」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4471c-109">For more information about a more comprehensive Outlook platform introduced in Outlook 2007 to reduce reliance on CDO and ECE, see [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span></span>

