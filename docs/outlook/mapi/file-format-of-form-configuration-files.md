---
title: フォーム構成ファイルの形式
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800044"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="ecec9-103">フォーム構成ファイルの形式</span><span class="sxs-lookup"><span data-stu-id="ecec9-103">File format of form configuration files</span></span>

<span data-ttu-id="ecec9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecec9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecec9-105">フォーム構成ファイルは、フォームを定義するのにはフォームの開発者によって作成された形式のファイルです。</span><span class="sxs-lookup"><span data-stu-id="ecec9-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="ecec9-106">フォーム構成ファイルが使用されるためフォーム マネージャーがフォームをロードするのには、フォーム構成ファイルを使用して、各フォームを定義しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ecec9-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="ecec9-107">フォーム構成ファイルには、.cfg ファイル名の拡張子が必要です。</span><span class="sxs-lookup"><span data-stu-id="ecec9-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="ecec9-108">ファイルは、Windows 初期化ファイル (.ini ファイル) の一般的な構文に依存します。</span><span class="sxs-lookup"><span data-stu-id="ecec9-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="ecec9-109">名前付きのセクションに分かれていて、各セクションには、一連エントリと値にはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ecec9-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="ecec9-110">次の種類のいずれかの値がある: 文字列、表示される文字列、文字列のプラットフォーム、パス、整数、またはグローバル一意識別子、 **GUID**です。</span><span class="sxs-lookup"><span data-stu-id="ecec9-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="ecec9-111">フォーム構成ファイルは、任意のテキスト エディターまたはテキスト形式で保存できるワード プロセッサで作成できます。</span><span class="sxs-lookup"><span data-stu-id="ecec9-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

