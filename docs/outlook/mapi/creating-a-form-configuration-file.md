---
title: フォーム構成ファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425219"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="ff0d4-103">フォーム構成ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="ff0d4-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="ff0d4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff0d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff0d4-105">フォーム構成ファイルは、使用するフォーム マネージャーとクライアント アプリケーションの両方にフォームに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="ff0d4-106">フォーム構成ファイルには、メッセージング クライアントで使用するためにフォームによって発行されたプロパティ、フォームによって実装された動詞、フォームでサポートされるプラットフォームなど、フォームの広範な仕様が含まれる。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="ff0d4-107">フォーム構成ファイルは、拡張子が .cfg のファイルで、初期化ファイルの形式とWindows形式です。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="ff0d4-108">これは、多数のセクションを含むプレーン テキスト ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="ff0d4-109">各セクションは、角かっこで囲まれたセクション名で始まります。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="ff0d4-110">各セクションには、そのセクションに関連する値と設定を定義する 1 つ以上の行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="ff0d4-111">値には、次のいずれかの種類があります。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="ff0d4-112">String</span><span class="sxs-lookup"><span data-stu-id="ff0d4-112">String</span></span>
    
- <span data-ttu-id="ff0d4-113">表示される文字列</span><span class="sxs-lookup"><span data-stu-id="ff0d4-113">Displayed string</span></span>
    
- <span data-ttu-id="ff0d4-114">プラットフォーム文字列</span><span class="sxs-lookup"><span data-stu-id="ff0d4-114">Platform string</span></span>
    
- <span data-ttu-id="ff0d4-115">パス名</span><span class="sxs-lookup"><span data-stu-id="ff0d4-115">Path name</span></span>
    
- <span data-ttu-id="ff0d4-116">整数</span><span class="sxs-lookup"><span data-stu-id="ff0d4-116">Integer</span></span>
    
- <span data-ttu-id="ff0d4-117">GUID</span><span class="sxs-lookup"><span data-stu-id="ff0d4-117">GUID</span></span>
    
<span data-ttu-id="ff0d4-118">.cfg ファイルのセクションの詳細については、「フォーム構成ファイルの [ファイル形式」を参照してください](file-format-of-form-configuration-files.md)。</span><span class="sxs-lookup"><span data-stu-id="ff0d4-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff0d4-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff0d4-119">See also</span></span>



[<span data-ttu-id="ff0d4-120">MAPI フォーム サーバーの開発</span><span class="sxs-lookup"><span data-stu-id="ff0d4-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

