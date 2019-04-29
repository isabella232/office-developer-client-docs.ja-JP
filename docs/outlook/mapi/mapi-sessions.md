---
title: MAPI セッション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c5a7c137-393e-40ff-a2b9-afe02da2435a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3dd55d8ee3cb2751fb27184f0069ae831e2164ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435874"
---
# <a name="mapi-sessions"></a><span data-ttu-id="6bad0-103">MAPI セッション</span><span class="sxs-lookup"><span data-stu-id="6bad0-103">MAPI sessions</span></span>

<span data-ttu-id="6bad0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bad0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bad0-105">��ɂȂ郁�b�Z�[�W���O �V�X�e���Ăяo���N���C�A���g �A�v���P�[�V�����ɂ́A�O�ɁA�Z�b�V�����A�܂��� MAPI �T�u�V�X�e���Ƃ̐ڑ���m������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="6bad0-105">Before the client application can call an underlying messaging system, it must establish a session, or connection, with the MAPI subsystem.</span></span>
  
<span data-ttu-id="6bad0-p101">���O�I������ƁA���[�U�[�A�L���ȃv���t�@�C���ɃA�N�Z�X���A���b�Z�[�W���O �V�X�e���ƃ��b�Z�[�W �T�[�r�X�̎��i����m�F����v���Z�X�́A�Z�b�V�������J�n����܂��B���ɁA�v���Z�X�ɂ��A���ׂẴv���t�@�C���̃��b�Z�[�W�̃T�[�r�X���������\������Ă��܂��B�N���C�A���g�̃C���^�[�t�F�C�X��g�p����ɂ́A���O�I���Ăяo�������܂�܂��BMAPI �N���C�A���g�ł́A [MAPILogonEx](mapilogonex.md)�֐���Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="6bad0-p101">Sessions are initiated when a user logs on, a process that accesses a valid profile and validates the messaging system and the message service credentials. Then, the process ensures that all of the profile's message services are correctly configured. The client interface you use determines the logon call. MAPI clients call the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
<span data-ttu-id="6bad0-p102">Message service configuration is one of the most important parts of the logon process. The profile is the initial source for configuration information. If information for a particular message service is missing, the logon process tries to prompt the user to supply it. This is not always successful for two reasons: First, prompting the user requires the display of a dialog box. It is possible for clients to disallow the display of a user interface by passing a flag into the logon call. Second, the user could cancel the dialog box before the needed information can be added.</span><span class="sxs-lookup"><span data-stu-id="6bad0-p102">Message service configuration is one of the most important parts of the logon process. The profile is the initial source for configuration information. If information for a particular message service is missing, the logon process tries to prompt the user to supply it. This is not always successful for two reasons: First, prompting the user requires the display of a dialog box. It is possible for clients to disallow the display of a user interface by passing a flag into the logon call. Second, the user could cancel the dialog box before the needed information can be added.</span></span>
  
<span data-ttu-id="6bad0-p103">When a logon process fails one time, the user is informed of the failure and given the chance to retry or correct the error condition. Once again, a user interface will be displayed, if the client allows it, and the user will be prompted to enter whatever data is missing. If this second try is unsuccessful, MAPI disables all service providers in the message service for the duration of the session. In effect, the whole message service is disabled. This means that none of the service providers in the message service can work. This is done because if one provider fails logon, the other providers usually also fail. The logon process can fail due to an invalid path for a necessary resource, an incompatible version of MAPI, an unavailable messaging server, or data corruption.</span><span class="sxs-lookup"><span data-stu-id="6bad0-p103">When a logon process fails one time, the user is informed of the failure and given the chance to retry or correct the error condition. Once again, a user interface will be displayed, if the client allows it, and the user will be prompted to enter whatever data is missing. If this second try is unsuccessful, MAPI disables all service providers in the message service for the duration of the session. In effect, the whole message service is disabled. This means that none of the service providers in the message service can work. This is done because if one provider fails logon, the other providers usually also fail. The logon process can fail due to an invalid path for a necessary resource, an incompatible version of MAPI, an unavailable messaging server, or data corruption.</span></span> 
  
<span data-ttu-id="6bad0-p104">�N���C�A���g�����O�I���ʘb��m������Z�b�V������ 2 ��ނ̂����ꂩ��w��ł��܂��B �X �̃Z�b�V�����܂��͋��L�̃Z�b�V�����B�X �̃Z�b�V�����̓v���C�x�[�g�ڑ����܂��B�N���C�A���g �A�v���P�[�V������g�p���Ă���Z�b�V�����̊Ԃ̈�Έꃊ���[�V�����V�b�v������܂��B���ʂƂ��āA�Z�b�V�����̋��L��N���C�A���g �A�v���P�[�V������v���t�@�C������L���܂��B���L�Z�b�V������ 1 ��m�����܂����A������g�p����K�v�����邻�̑��̃N���C�A���g �A�v���P�[�V�����Ŏg�p���邱�Ƃ��ł��܂��B�v���t�@�C������ю��i���́A�ŏ��̃��O�I���݂̂�w�肵�܂��B</span><span class="sxs-lookup"><span data-stu-id="6bad0-p104">Clients can specify one of two types of sessions to be established in the logon call: an individual session or a shared session. Individual sessions are private connections; there is a one-to-one relationship between a client application and the session it is using. As a consequence, client applications that share a session also share a profile. Shared sessions are established once but can be used by other client applications that need to use them. The profile and credentials are specified only with the initial logon.</span></span> 
  
<span data-ttu-id="6bad0-p105">Clients can log on multiple times as the same user or as multiple users. MAPI does not prevent this. Some service providers, however, might not be as flexible, returning the error value MAPI_E_SESSION_LIMIT on subsequent logon attempts. Service providers with underlying hardware limitations can be required to enforce a session limit.</span><span class="sxs-lookup"><span data-stu-id="6bad0-p105">Clients can log on multiple times as the same user or as multiple users. MAPI does not prevent this. Some service providers, however, might not be as flexible, returning the error value MAPI_E_SESSION_LIMIT on subsequent logon attempts. Service providers with underlying hardware limitations can be required to enforce a session limit.</span></span>
  
<span data-ttu-id="6bad0-p106">The function calls for establishing a session have a collection of flags and parameters that control how the session is created. The client specifies an optional profile name and a window handle that acts as the parent window for any dialog boxes that are displayed. The flags include MAPI_NEW_SESSION, which requests that a new, individual session (rather than a shared session) be established, and the MAPI_LOGON_UI user interface flag. The user interface flag is set to request a logon dialog box.</span><span class="sxs-lookup"><span data-stu-id="6bad0-p106">The function calls for establishing a session have a collection of flags and parameters that control how the session is created. The client specifies an optional profile name and a window handle that acts as the parent window for any dialog boxes that are displayed. The flags include MAPI_NEW_SESSION, which requests that a new, individual session (rather than a shared session) be established, and the MAPI_LOGON_UI user interface flag. The user interface flag is set to request a logon dialog box.</span></span>
  
<span data-ttu-id="6bad0-136">���̐}�́A�����̂��܂��܂ȃp�����[�^�[�ƃt���O�� MAPI �Z�b�V������m��������@������܂��B</span><span class="sxs-lookup"><span data-stu-id="6bad0-136">The following illustration shows how these various parameters and flags establish a MAPI session.</span></span>
  
<span data-ttu-id="6bad0-137">**MAPI �Z�b�V�����̃t���[�\`���[�g**</span><span class="sxs-lookup"><span data-stu-id="6bad0-137">**MAPI session flowchart**</span></span>
  
<span data-ttu-id="6bad0-138">![MAPI セッションのフローチャート](media/amapi_47.gif "MAPI セッションのフローチャート")</span><span class="sxs-lookup"><span data-stu-id="6bad0-138">![MAPI session flowchart](media/amapi_47.gif "MAPI session flowchart")</span></span>
  
<span data-ttu-id="6bad0-139">�N���C�A���g �A�v���P�[�V���������Z�b�V�����̏������@�̏ڍׂɂ��ẮA [MAPI �Z�b�V�����̏���](mapi-session-handling.md)��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="6bad0-139">For information about handling sessions from within a client application, see [MAPI Session Handling](mapi-session-handling.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6bad0-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="6bad0-140">See also</span></span>

- [<span data-ttu-id="6bad0-141">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="6bad0-141">MAPILogonEx</span></span>](mapilogonex.md)  
- [<span data-ttu-id="6bad0-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bad0-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)
- [<span data-ttu-id="6bad0-143">MAPI �Z�b�V�����̏���</span><span class="sxs-lookup"><span data-stu-id="6bad0-143">MAPI Session Handling</span></span>](mapi-session-handling.md)  
- [<span data-ttu-id="6bad0-144">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="6bad0-144">MAPI Programming Overview</span></span>](mapi-programming-overview.md)

