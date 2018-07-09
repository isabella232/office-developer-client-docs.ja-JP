---
title: Round 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: 指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798735"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="778f1-103">Round 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="778f1-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="778f1-104">指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。</span><span class="sxs-lookup"><span data-stu-id="778f1-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="778f1-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="778f1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="778f1-107">構文</span><span class="sxs-lookup"><span data-stu-id="778f1-107">Syntax</span></span>

 <span data-ttu-id="778f1-108">**ラウンド**(*番号*、*有効桁数*は、[ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="778f1-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="778f1-109">**Round** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="778f1-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="778f1-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="778f1-110">**Argument name**</span></span>|<span data-ttu-id="778f1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="778f1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="778f1-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="778f1-112">*Number*</span></span>  <br/> |<span data-ttu-id="778f1-113">数値式を指定します。</span><span class="sxs-lookup"><span data-stu-id="778f1-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="778f1-114">*精度*</span><span class="sxs-lookup"><span data-stu-id="778f1-114">*Precision*</span></span>  <br/> |<span data-ttu-id="778f1-115">精度*数値*が丸められます。</span><span class="sxs-lookup"><span data-stu-id="778f1-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="778f1-116">*有効桁数*は、数値式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="778f1-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="778f1-117">*精度*が正の数値の場合は、長さが指定した 10 進数の位置の数に*数値*が丸められます。</span><span class="sxs-lookup"><span data-stu-id="778f1-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="778f1-118">*有効桁数*に負の数がある場合は、長さの指定に従って、小数点の左側にある*数値*が丸められます。</span><span class="sxs-lookup"><span data-stu-id="778f1-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="778f1-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="778f1-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="778f1-120">実行する操作の種類。</span><span class="sxs-lookup"><span data-stu-id="778f1-120">The type of operation to perform.</span></span> <span data-ttu-id="778f1-121">省略すると 0 に設定、*数値*が丸められます。</span><span class="sxs-lookup"><span data-stu-id="778f1-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="778f1-122">0 以外の値を指定すると、*番号*が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="778f1-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="778f1-123">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="778f1-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="778f1-124">注釈</span><span class="sxs-lookup"><span data-stu-id="778f1-124">Remarks</span></span>

 <span data-ttu-id="778f1-p104">**Round** は常に値を返します。長さが負の値であり、少数点よりも前の桁数よりも大きい場合、 **Round** は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="778f1-p104">**Round** always returns a value. If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

