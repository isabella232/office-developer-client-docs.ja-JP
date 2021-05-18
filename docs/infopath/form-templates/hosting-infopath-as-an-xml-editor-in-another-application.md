---
title: InfoPath を別のアプリケーションで XML エディターとしてホストする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Microsoft InfoPath のフォーム編集環境は、カスタム Windows アプリケーションでホストすることができます。その場合、開発者は InfoPath のフォーム編集環境を基幹業務アプリケーションに統合できます。
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422580"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="59a8c-103">InfoPath を別のアプリケーションで XML エディターとしてホストする</span><span class="sxs-lookup"><span data-stu-id="59a8c-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="59a8c-p101">Microsoft InfoPath フォームの編集環境は、カスタムの Windows アプリケーションでホストできます。開発者はこの機能を利用して、InfoPath フォームの編集環境を基幹業務アプリケーションに統合できます。従来型 COM ベース アプリケーションの開発者は、IPEDITOR.DLL を参照する方法で **InfoPathEditorObject** オブジェクトを使用できます。Microsoft .NET ベース アプリケーションの開発者は、COM インターフェイスに基づくマネージ型を提供する **Microsoft.Office.InfoPath.FormControl** アセンブリを使用できます。IPEDITOR.DLL および **Microsoft.Office.InfoPath.FormControl** アセンブリは両方とも InfoPath と一緒に C:\Program Files\Microsoft Office\Office15 または C:\Program Files (x86)\Microsoft Office\Office15 フォルダーにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="59a8c-p101">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application. This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications. Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface. The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="59a8c-108">MSDN の記事「カスタム Windows フォーム アプリケーションで InfoPath 2007 フォーム編集環境をホストする」では、**FormControl** オブジェクトと、このオブジェクトをカスタムの .NET ベース アプリケーションに統合する方法について解説しています。</span><span class="sxs-lookup"><span data-stu-id="59a8c-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="59a8c-109">この記事に関連するダウンロード パッケージには、InfoPath フォームの編集環境を COM **IOleCommandTargets** を使用して再現する .NET 関数を提供するカスタム アプリケーションが収録されています。</span><span class="sxs-lookup"><span data-stu-id="59a8c-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

