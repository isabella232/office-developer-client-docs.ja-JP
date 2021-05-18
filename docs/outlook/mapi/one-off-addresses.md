---
title: 一時アドレス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409112"
---
# <a name="one-off-addresses"></a><span data-ttu-id="06997-103">一時アドレス</span><span class="sxs-lookup"><span data-stu-id="06997-103">One-off addresses</span></span>

<span data-ttu-id="06997-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06997-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06997-105">1 回のアドレスは、セッションのアドレス帳コンテナーに対応するエントリを持つ受信者である 1 回の受信者にメッセージを送信するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="06997-105">One-off addresses are used to send messages to one-off recipients, recipients that do not have a corresponding entry in any of the session's address book containers.</span></span> <span data-ttu-id="06997-106">クライアントは、アドレス帳に新しいエントリを追加したり、新しい受信者を送信メッセージの受信者リストに追加したりすると、1 回きりアドレスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="06997-106">Clients can create one-off addresses when they add new entries to the address book or new recipients to the recipient list of an outgoing message.</span></span> <span data-ttu-id="06997-107">1 回のアドレスは、変更可能な任意のコンテナーに追加できます。</span><span class="sxs-lookup"><span data-stu-id="06997-107">One-off addresses can be added to any container that is modifiable.</span></span>
  
<span data-ttu-id="06997-108">1 回のアドレスを作成するために、クライアントは編集コントロールを含む特別なテンプレートを使用して、1 回きりアドレスを構成する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="06997-108">To create a one-off address, clients use a special template containing edit controls for entering all of the information that makes up a one-off address.</span></span> <span data-ttu-id="06997-109">1 回のアドレス (他の種類のアドレスなど) は、定義済みの形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="06997-109">One-off addresses, like addresses of other types, use a predefined format.</span></span> <span data-ttu-id="06997-110">1 回限りアドレス形式は、MAPI によって次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="06997-110">The one-off address format is defined by MAPI as follows:</span></span>
  
`Display name[Address type:Email address]`
  
<span data-ttu-id="06997-111">この形式には 6 つのコンポーネントと、文字の引用に関する規則があります。</span><span class="sxs-lookup"><span data-stu-id="06997-111">There are six components to this format and some rules about quoting characters.</span></span> <span data-ttu-id="06997-112">コンポーネントについては、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="06997-112">The components are described in the following table.</span></span>
  
|<span data-ttu-id="06997-113">**コンポーネント**</span><span class="sxs-lookup"><span data-stu-id="06997-113">**Component**</span></span>|<span data-ttu-id="06997-114">**使用法**</span><span class="sxs-lookup"><span data-stu-id="06997-114">**Usage**</span></span>|<span data-ttu-id="06997-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="06997-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="06997-116">表示名</span><span class="sxs-lookup"><span data-stu-id="06997-116">Display name</span></span>  <br/> |<span data-ttu-id="06997-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="06997-117">Optional</span></span>  <br/> |<span data-ttu-id="06997-118">存在しない場合 **、IAddrBook::ResolveName は** 電子メール アドレスの表示部分を表示名として使用します。</span><span class="sxs-lookup"><span data-stu-id="06997-118">If not present, **IAddrBook::ResolveName** uses the visible part of the email address as the display name.</span></span> <span data-ttu-id="06997-119">空白が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="06997-119">May include blanks.</span></span> <span data-ttu-id="06997-120">詳細については [、「IAddrBook::ResolveName」を参照してください](iaddrbook-resolvename.md)。</span><span class="sxs-lookup"><span data-stu-id="06997-120">For more information, see [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>  <br/> |
|<span data-ttu-id="06997-121">[</span><span class="sxs-lookup"><span data-stu-id="06997-121">[</span></span>  <br/> |<span data-ttu-id="06997-122">必須</span><span class="sxs-lookup"><span data-stu-id="06997-122">Required</span></span>  <br/> |<span data-ttu-id="06997-123">型とアドレスの情報の開始を示します。</span><span class="sxs-lookup"><span data-stu-id="06997-123">Delineates the start of the type and address information.</span></span>  <br/> |
|<span data-ttu-id="06997-124">]</span><span class="sxs-lookup"><span data-stu-id="06997-124">]</span></span>  <br/> |<span data-ttu-id="06997-125">必須</span><span class="sxs-lookup"><span data-stu-id="06997-125">Required</span></span>  <br/> |<span data-ttu-id="06997-126">型とアドレスの情報の末尾を示します。</span><span class="sxs-lookup"><span data-stu-id="06997-126">Delineates the end of the type and address information.</span></span> <span data-ttu-id="06997-127">空白以外の文字が続く場合、エントリはカスタム受信者として扱われます。</span><span class="sxs-lookup"><span data-stu-id="06997-127">If anything other than white space follows this character, the entry is not treated as a custom recipient.</span></span>  <br/> |
|<span data-ttu-id="06997-128">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="06997-128">Address type</span></span>  <br/> |<span data-ttu-id="06997-129">必須</span><span class="sxs-lookup"><span data-stu-id="06997-129">Required</span></span>  <br/> |<span data-ttu-id="06997-130">アドレスの種類。は、特定のアドレス形式にマップされます。</span><span class="sxs-lookup"><span data-stu-id="06997-130">Type of address; maps to a specific address format.</span></span> <span data-ttu-id="06997-131">詳細については、「MAPI アドレスの [種類」を参照してください](mapi-address-types.md)。</span><span class="sxs-lookup"><span data-stu-id="06997-131">For more information, see [MAPI Address Types](mapi-address-types.md).</span></span>  <br/> |
|<span data-ttu-id="06997-132">:</span><span class="sxs-lookup"><span data-stu-id="06997-132">:</span></span>  <br/> |<span data-ttu-id="06997-133">必須</span><span class="sxs-lookup"><span data-stu-id="06997-133">Required</span></span>  <br/> |<span data-ttu-id="06997-134">アドレスの種類と電子メール アドレスを分離します。</span><span class="sxs-lookup"><span data-stu-id="06997-134">Separates the address type from the email address.</span></span>  <br/> |
|<span data-ttu-id="06997-135">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="06997-135">Email address</span></span>  <br/> |<span data-ttu-id="06997-136">必須</span><span class="sxs-lookup"><span data-stu-id="06997-136">Required</span></span>  <br/> |<span data-ttu-id="06997-137">��M�҂̃A�h���X�ł��B</span><span class="sxs-lookup"><span data-stu-id="06997-137">Address of the recipient.</span></span> <span data-ttu-id="06997-138">空白が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="06997-138">May include blanks.</span></span>  <br/> |
   
<span data-ttu-id="06997-139">MAPI では、特定の引用符付き文字セットを使用して、アドレスにコンマ (,,)、左かっこ ([)、コロン (:)) などの特殊文字を含めることができます。改行や改行などの型指定できない文字や、他の 16 進数に相当する文字があります。</span><span class="sxs-lookup"><span data-stu-id="06997-139">MAPI uses particular sets of quoting characters to allow addresses to contain special characters such as comma (,), left bracket ([), and colon (:) and some untypeable characters such as the carriage return or line feed or any other hexadecimal equivalent.</span></span> <span data-ttu-id="06997-140">引用文字は円記号 ( です \) 。</span><span class="sxs-lookup"><span data-stu-id="06997-140">The quoting character is the backslash (\).</span></span> <span data-ttu-id="06997-141">したがって、クライアントまたはプロバイダーがアドレスに円記号を挿入する必要がある場合は、引用文字 (" ") を使用して、バックスラッシュを事前に設定する必要 \\ があります。</span><span class="sxs-lookup"><span data-stu-id="06997-141">Therefore, if clients or providers must insert a backslash in an address, they must preceed it with the quoting character ("\\").</span></span>
  
<span data-ttu-id="06997-142">クライアントとサービス プロバイダーは、固定されていない型指定可能なフィールドで、この引用手法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06997-142">Clients and service providers can use this quoting technique in any of the nonfixed, typeable fields.</span></span> <span data-ttu-id="06997-143">たとえば、次のエントリは、表示名として Bill Lee、アドレスの種類として MSPEER、電子メール アドレスとして \\ billll\in に変換されます。</span><span class="sxs-lookup"><span data-stu-id="06997-143">For example, the following entry translates to Bill Lee as the display name, MSPEER as the address type, and \\billll\in as the email address:</span></span>
  
`Bill Lee[MSPEER:\\\\billl\in]`

<span data-ttu-id="06997-144">特殊な型指定できない文字を挿入するために、クライアントとサービス プロバイダーは、16 進数に相当する数値を表す引用符文字の後に x と 2 の 16 進数字を使用します。</span><span class="sxs-lookup"><span data-stu-id="06997-144">To insert special nontypeable characters, clients and service providers use a quoting character followed by an x and two hexadecimal digits to represent their hexadecimal equivalent.</span></span> <span data-ttu-id="06997-145">たとえば、アドレスにキャリッジ リターン (\0d) を 16 進数で表す型指定できない文字がある場合、クライアントは次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="06997-145">For example, if an address has a nontypeable character that equates to a carriage return, (\0d) in hexadecimal, a client would enter them as:</span></span>
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

<span data-ttu-id="06997-146">**IAddrBook::ResolveName** は、ほとんどの SMTP アドレスを自動的に解析し、次の形式のアドレスを探します。</span><span class="sxs-lookup"><span data-stu-id="06997-146">**IAddrBook::ResolveName** also automatically parses most SMTP addresses, looking for addresses with the following format:</span></span> 
  
`XXX@YYY.ZZZ`

<span data-ttu-id="06997-147">可能なすべての RFC822 形式が処理されるとは限りありませんが、ほとんどのユーザーにとってこの自動解析は適切です。</span><span class="sxs-lookup"><span data-stu-id="06997-147">Although not all of the possible RFC822 formats are handled, this automatic parsing is adequate for most users.</span></span> <span data-ttu-id="06997-148">**ResolveName** には、ユーザーがメッセージに SMTP アドレスを直接入力し、そのメッセージをインターネット ユーザーに送信するためのこの機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06997-148">**ResolveName** includes this functionality to enable users to enter SMTP addresses directly into a message and have that message go to the Internet user.</span></span> <span data-ttu-id="06997-149">アドレスの XXX、YYY、および ZZZ コンポーネントには、1 つ以上の文字を指定できます。</span><span class="sxs-lookup"><span data-stu-id="06997-149">The XXX, YYY, and ZZZ components of the address can be one or more characters.</span></span> <span data-ttu-id="06997-150">AT 記号 (@) は XXX、YYY、または ZZZ アドレス コンポーネントに含めず、YYY コンポーネントにはピリオドを含めません。</span><span class="sxs-lookup"><span data-stu-id="06997-150">The at sign (@) cannot be included in either the XXX, YYY, or ZZZ address components and the YYY component also cannot include the period.</span></span> <span data-ttu-id="06997-151">次の文字は SMTP アドレスの特殊文字なので、MAPI は自動的にこれらの文字を含む表示名を 1 回のアドレスに変換します。</span><span class="sxs-lookup"><span data-stu-id="06997-151">Because the following characters are special characters in SMTP addresses, MAPI automatically converts a display name containing these characters into a one-off address:</span></span> 
  
- \>\>
    
- @
    
- \<\>
    
- <span data-ttu-id="06997-152">.</span><span class="sxs-lookup"><span data-stu-id="06997-152">.</span></span>
    
<span data-ttu-id="06997-153">すべての 1 回のアドレスには、対応する 1 回分のエントリ識別子が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="06997-153">Every one-off address is assigned a corresponding one-off entry identifier.</span></span> <span data-ttu-id="06997-154">この割り当てを行う場合、クライアントは **IAddrBook::CreateOneOff** を呼び出し、トランスポート プロバイダーは **IMAPISupport::CreateOneOff を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="06997-154">To make this assignment, clients call **IAddrBook::CreateOneOff** and transport providers call **IMAPISupport::CreateOneOff**.</span></span> <span data-ttu-id="06997-155">詳細については [、「IAddrBook::CreateOneOff」](iaddrbook-createoneoff.md) および [「IMAPISupport::CreateOneOff」を参照してください](imapisupport-createoneoff.md)。</span><span class="sxs-lookup"><span data-stu-id="06997-155">For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).</span></span> <span data-ttu-id="06997-156">受信メッセージを処理する場合、トランスポート プロバイダーは、ゲートウェイ アドレスと、トランスポートの関連付けられたアドレス帳プロバイダーでは処理できないアドレスの 1 回のエントリ識別子を作成します。</span><span class="sxs-lookup"><span data-stu-id="06997-156">When processing incoming messages, transport providers create one-off entry identifiers for gateway addresses and for addresses that cannot be handled by the transport's associated address book providers.</span></span> <span data-ttu-id="06997-157">トランスポート プロバイダーは、メッセージ内の各アドレスの種類をチェックして、トランスポートに関連付けられたアドレス帳プロバイダーが処理できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="06997-157">Transport providers check the type of each address in a message to determine if it can be handled by an address book provider associated with the transport.</span></span> <span data-ttu-id="06997-158">できない場合、トランスポート プロバイダーは **IMAPISupport::CreateOneOff** を呼び出して、アドレスを 1 回のエントリ識別子に関連付ける。</span><span class="sxs-lookup"><span data-stu-id="06997-158">If it cannot, transport providers call **IMAPISupport::CreateOneOff** to associate the address with a one-off entry identifier.</span></span> 
  
<span data-ttu-id="06997-159">1 回のエントリ識別子には、次の順序で次の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="06997-159">One-off entry identifiers include the following information in the following order:</span></span>
  
1. <span data-ttu-id="06997-160">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="06997-160">**MAPIUID**</span></span>
    
2. <span data-ttu-id="06997-161">バージョン</span><span class="sxs-lookup"><span data-stu-id="06997-161">Version</span></span>
    
3. <span data-ttu-id="06997-162">フラグ</span><span class="sxs-lookup"><span data-stu-id="06997-162">Flags</span></span>
    
4. <span data-ttu-id="06997-163">表示名</span><span class="sxs-lookup"><span data-stu-id="06997-163">Display name</span></span>
    
5. <span data-ttu-id="06997-164">アドレスの種類</span><span class="sxs-lookup"><span data-stu-id="06997-164">Address type</span></span>
    
6. <span data-ttu-id="06997-165">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="06997-165">Email address</span></span>
    
<span data-ttu-id="06997-166">**IAddrBook::CreateOneOff** と **IMAPISupport::CreateOneOff** の呼び出しでは、クライアントとトランスポート プロバイダーは、1 回のアドレスで表される受信者が書式設定されたテキストまたは埋め込み OLE オブジェクトを処理できるかどうかを示すフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="06997-166">In the calls to **IAddrBook::CreateOneOff** and **IMAPISupport::CreateOneOff**, clients and transport providers can set a flag that indicates whether or not the recipient represented by the one-off address can process formatted text or embedded OLE objects.</span></span> <span data-ttu-id="06997-167">受信者が書式設定されたテキストおよび OLE オブジェクトを処理できると示すために、クライアントとトランスポート プロバイダーは  _ulFlags_ パラメーターに MAPI_SEND_NO_RICH_INFOフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="06997-167">To indicate that a recipient can handle formatted text and OLE objects, clients and transport providers set the MAPI_SEND_NO_RICH_INFO flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="06997-168">MAPI は、1 回の受信者のPR_SEND_RICH_INFO **(** [PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="06997-168">MAPI then sets the one-off recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="06997-169">このフラグを設定しない場合、1 回 **限** PR_SEND_RICH_INFOアドレスが SMTP アドレスとして解釈されない限り、MAPI は TRUE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="06997-169">When this flag is not set, MAPI sets **PR_SEND_RICH_INFO** to TRUE unless the one-off address is interpreted as an SMTP address.</span></span> <span data-ttu-id="06997-170">この 1 つのケースでは **、既定PR_SEND_RICH_INFO** FALSE になります。</span><span class="sxs-lookup"><span data-stu-id="06997-170">In this one case, **PR_SEND_RICH_INFO** defaults to FALSE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06997-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="06997-171">See also</span></span>

- [<span data-ttu-id="06997-172">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="06997-172">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)

