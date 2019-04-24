---
title: フォーム構成ファイルを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333020"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="be6df-103">フォーム構成ファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="be6df-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="be6df-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be6df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be6df-105">フォーム構成ファイルは、使用されているフォームマネージャーとクライアントアプリケーションの両方のフォームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="be6df-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="be6df-106">フォーム構成ファイルには、フォームについての詳細な仕様が含まれています。これには、メッセージングクライアントで使用するためにフォームによって発行されるプロパティ、フォームによって実装される動詞、フォームでサポートされているプラットフォームが含まれます。</span><span class="sxs-lookup"><span data-stu-id="be6df-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="be6df-107">フォーム構成ファイルは、拡張子が cfg のファイルで、Windows 初期化ファイルに似た形式になっています。</span><span class="sxs-lookup"><span data-stu-id="be6df-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="be6df-108">これは、いくつかのセクションがあるプレーンテキストファイルです。</span><span class="sxs-lookup"><span data-stu-id="be6df-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="be6df-109">各セクションは、角かっこで囲まれたセクション名で始まります。</span><span class="sxs-lookup"><span data-stu-id="be6df-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="be6df-110">各セクションには、そのセクションに関連する値と設定を定義する1つまたは複数の行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="be6df-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="be6df-111">値の型は次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="be6df-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="be6df-112">String</span><span class="sxs-lookup"><span data-stu-id="be6df-112">String</span></span>
    
- <span data-ttu-id="be6df-113">表示される文字列</span><span class="sxs-lookup"><span data-stu-id="be6df-113">Displayed string</span></span>
    
- <span data-ttu-id="be6df-114">プラットフォーム文字列</span><span class="sxs-lookup"><span data-stu-id="be6df-114">Platform string</span></span>
    
- <span data-ttu-id="be6df-115">パス名</span><span class="sxs-lookup"><span data-stu-id="be6df-115">Path name</span></span>
    
- <span data-ttu-id="be6df-116">整数</span><span class="sxs-lookup"><span data-stu-id="be6df-116">Integer</span></span>
    
- <span data-ttu-id="be6df-117">GUID</span><span class="sxs-lookup"><span data-stu-id="be6df-117">GUID</span></span>
    
<span data-ttu-id="be6df-118">cfg ファイルのセクションの詳細については、「[フォーム構成ファイルのファイル形式](file-format-of-form-configuration-files.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be6df-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be6df-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="be6df-119">See also</span></span>



[<span data-ttu-id="be6df-120">MAPI フォームサーバーの開発</span><span class="sxs-lookup"><span data-stu-id="be6df-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

