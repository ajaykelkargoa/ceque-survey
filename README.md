<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Thinking Partners Survey</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif; line-height: 1.6; color: #4a4a4a; background-color: #fafafa; padding: 20px; }
        .container { max-width: 700px; margin: 20px auto; background: white; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.05); border: 1px solid #e8e8e8; }
        .header { padding: 32px 40px 24px; border-bottom: 1px solid #f0f0f0; text-align: center; }
        .title { font-size: 24px; font-weight: 600; color: #2d3748; margin-bottom: 8px; }
        .subtitle { font-size: 14px; color: #718096; margin-bottom: 16px; }
        .description { font-size: 16px; color: #4a5568; line-height: 1.5; }
        .form-container { padding: 32px 40px; }
        .question-group { margin-bottom: 32px; }
        .question-label { font-size: 16px; font-weight: 500; color: #2d3748; margin-bottom: 12px; display: block; }
        .required { color: #e53e3e; }
        .question-help { font-size: 14px; color: #718096; margin-bottom: 16px; font-style: italic; }
        .radio-group { margin-bottom: 16px; }
        .radio-option { display: flex; align-items: flex-start; margin-bottom: 12px; padding: 8px; border-radius: 4px; transition: background-color 0.2s ease; }
        .radio-option:hover { background-color: #f7fafc; }
        .radio-option input[type="radio"] { margin-right: 12px; margin-top: 2px; accent-color: #4299e1; }
        .radio-text { flex: 1; font-size: 14px; color: #4a5568; line-height: 1.4; }
        .text-input { width: 100%; padding: 12px 16px; border: 1px solid #d1d5db; border-radius: 6px; font-size: 14px; color: #374151; background-color: #ffffff; transition: border-color 0.2s ease; }
        .text-input:focus { outline: none; border-color: #4299e1; box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.1); }
        .textarea { min-height: 80px; resize: vertical; }
        .select-input { width: 100%; padding: 12px 16px; border: 1px solid #d1d5db; border-radius: 6px; font-size: 14px; color: #374151; background-color: #ffffff; cursor: pointer; }
        .select-input:focus { outline: none; border-color: #4299e1; box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.1); }
        .submit-section { padding: 24px 40px; border-top: 1px solid #f0f0f0; text-align: center; }
        .submit-button { background-color: #4299e1; color: white; padding: 14px 32px; border: none; border-radius: 6px; font-size: 16px; font-weight: 500; cursor: pointer; transition: background-color 0.2s ease; }
        .submit-button:hover { background-color: #3182ce; }
        .validation-error { color: #e53e3e; font-size: 14px; margin-top: 8px; }
        .success-message { background-color: #f0fff4; border: 1px solid #9ae6b4; color: #276749; padding: 16px; border-radius: 6px; margin-bottom: 24px; text-align: center; }
        @media (max-width: 640px) { .container { margin: 10px; } .header, .form-container, .submit-section { padding-left: 24px; padding-right: 24px; } }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1 class="title">AI Thinking Partners Survey</h1>
            <p class="subtitle">Pre-Session Survey for Muktangan Functional Heads</p>
            <p class="description">This survey serves two purposes: <strong>gathering your perspectives on AI and strategic thinking</strong>, and <strong>helping us plan a focused 60-minute session</strong> that addresses your specific needs and challenges. Your responses will shape both the content and examples we use to make our time together as valuable as possible.</p>
            <div style="background-color: #f0f8ff; border: 1px solid #b3d9ff; border-radius: 4px; padding: 12px; margin-top: 16px; font-size: 14px; color: #1a365d;">
                <strong>🔒 Confidentiality:</strong> All responses are confidential and will be used solely for session planning and content customization. Individual responses will not be shared publicly.
            </div>
        </div>
        
        <form id="surveyForm" class="form-container">
            <div class="question-group">
                <label class="question-label" for="name">Your Name <span class="required">*</span></label>
                <input type="text" id="name" name="name" class="text-input" required>
                <div class="validation-error" id="name-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label" for="department">Your Department at Muktangan <span class="required">*</span></label>
                <select id="department" name="department" class="select-input" required>
                    <option value="">Select your department</option>
                    <option value="fundraising">Fundraising and Partnerships</option>
                    <option value="academics">Academics</option>
                    <option value="systems">Systems and Tech</option>
                    <option value="communications">Communications</option>
                    <option value="monitoring">Monitoring and Evaluation</option>
                    <option value="programs">Programs</option>
                    <option value="hr_finance">HR and Finance</option>
                </select>
                <div class="validation-error" id="department-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label">How do you currently use AI tools? <span class="required">*</span></label>
                <div class="radio-group">
                    <div class="radio-option">
                        <input type="radio" id="exp1" name="aiExperience" value="no_experience" required>
                        <label for="exp1" class="radio-text">Haven't started - No experience with AI tools yet</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="exp2" name="aiExperience" value="basic" required>
                        <label for="exp2" class="radio-text">Basic user - Simple questions, take answers as-is</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="exp3" name="aiExperience" value="engaged" required>
                        <label for="exp3" class="radio-text">Engaged user - Provide detailed context, refine prompts based on results</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="exp4" name="aiExperience" value="strategic" required>
                        <label for="exp4" class="radio-text">Strategic user - Use AI for thinking through complex problems</label>
                    </div>
                </div>
                <div class="validation-error" id="aiExperience-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label" for="frustrations">If you use AI, what frustrates you most about it?</label>
                <p class="question-help">Optional - helps us address common pain points</p>
                <textarea id="frustrations" name="frustrations" class="text-input textarea" placeholder="Share your experience..."></textarea>
            </div>
            
            <div class="question-group">
                <label class="question-label">Your biggest thinking/communication challenge at work: <span class="required">*</span></label>
                <div class="radio-group">
                    <div class="radio-option">
                        <input type="radio" id="chal1" name="primaryChallenge" value="clarity" required>
                        <label for="chal1" class="radio-text">Clarity - Organizing messy ideas into clear, actionable structure</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="chal2" name="primaryChallenge" value="perspective" required>
                        <label for="chal2" class="radio-text">Perspective - Seeing problems from multiple stakeholder angles</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="chal3" name="primaryChallenge" value="depth" required>
                        <label for="chal3" class="radio-text">Depth - Moving beyond surface solutions to strategic insights</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="chal4" name="primaryChallenge" value="blindspots" required>
                        <label for="chal4" class="radio-text">Blind spots - Catching assumptions and gaps I might be missing</label>
                    </div>
                </div>
                <div class="validation-error" id="primaryChallenge-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label" for="example">Give us a specific example from your work: <span class="required">*</span></label>
                <p class="question-help">This helps us create relevant demos - e.g., "Deciding between scaling programs vs deepening impact in current areas"</p>
                <textarea id="example" name="example" class="text-input textarea" placeholder="Describe a specific situation..." required></textarea>
                <div class="validation-error" id="example-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label">What would make these 60 minutes valuable for you? <span class="required">*</span></label>
                <div class="radio-group">
                    <div class="radio-option">
                        <input type="radio" id="goal1" name="sessionGoal" value="framework" required>
                        <label for="goal1" class="radio-text">Framework - A clear methodology I can use repeatedly</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="goal2" name="sessionGoal" value="mindset" required>
                        <label for="goal2" class="radio-text">Mindset shift - Understanding AI as strategic thinking partner</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="goal3" name="sessionGoal" value="practical" required>
                        <label for="goal3" class="radio-text">Practical skills - Immediate tools for my daily work challenges</label>
                    </div>
                    <div class="radio-option">
                        <input type="radio" id="goal4" name="sessionGoal" value="strategic" required>
                        <label for="goal4" class="radio-text">Strategic insight - How this enhances Muktangan's mission impact</label>
                    </div>
                </div>
                <div class="validation-error" id="sessionGoal-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label" for="outcome">One thing you hope to walk away knowing: <span class="required">*</span></label>
                <p class="question-help">What specific outcome would make this session worthwhile?</p>
                <textarea id="outcome" name="outcome" class="text-input textarea" placeholder="What do you want to learn or achieve..." required></textarea>
                <div class="validation-error" id="outcome-error"></div>
            </div>
            
            <div class="question-group">
                <label class="question-label" for="context">Anything specific about AI/prompting that concerns or excites you?</label>
                <p class="question-help">Optional - helps us address expectations and interests</p>
                <textarea id="context" name="context" class="text-input textarea" placeholder="Share your thoughts..."></textarea>
            </div>
        </form>
        
        <div class="submit-section">
            <button type="submit" form="surveyForm" class="submit-button" id="submitBtn">Submit Survey</button>
        </div>
    </div>

    <script>
        let responses = JSON.parse(localStorage.getItem('surveyResponses') || '[]');
        
        document.getElementById('surveyForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            document.querySelectorAll('.validation-error').forEach(error => {
                error.textContent = '';
            });
            
            let isValid = true;
            const formData = new FormData(this);
            const data = {};
            
            const requiredFields = ['name', 'department', 'aiExperience', 'primaryChallenge', 'example', 'sessionGoal', 'outcome'];
            
            for (let field of requiredFields) {
                const value = formData.get(field);
                if (!value || value.trim() === '') {
                    document.getElementById(field + '-error').textContent = 'This field is required';
                    isValid = false;
                } else {
                    data[field] = value.trim();
                }
            }
            
            data.frustrations = formData.get('frustrations') || '';
            data.context = formData.get('context') || '';
            data.timestamp = new Date().toISOString();
            
            if (!isValid) return;
            
            responses.push(data);
            localStorage.setItem('surveyResponses', JSON.stringify(responses));
            
            const successMsg = document.createElement('div');
            successMsg.className = 'success-message';
            successMsg.textContent = 'Thank you! Your response has been recorded. We look forward to tailoring the session to your needs.';
            
            const formContainer = document.querySelector('.form-container');
            formContainer.insertBefore(successMsg, formContainer.firstChild);
            
            this.reset();
            document.getElementById('submitBtn').textContent = 'Submit Another Response';
        });
        
        window.showAdmin = function() {
            if (responses.length === 0) {
                alert('No responses yet');
                return;
            }
            const csvContent = [
                ['Name', 'Department', 'AI Experience', 'Frustrations', 'Primary Challenge', 'Example', 'Session Goal', 'Learning Outcome', 'Additional Context', 'Timestamp'].join(','),
                ...responses.map(r => [
                    `"${r.name}"`, `"${r.department}"`, `"${r.aiExperience}"`, `"${r.frustrations}"`,
                    `"${r.primaryChallenge}"`, `"${r.example}"`, `"${r.sessionGoal}"`, `"${r.outcome}"`,
                    `"${r.context}"`, `"${r.timestamp}"`
                ].join(','))
            ].join('\n');
            
            const blob = new Blob([csvContent], { type: 'text/csv' });
            const url = window.URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'survey-responses.csv';
            a.click();
            window.URL.revokeObjectURL(url);
            
            console.log('Responses:', responses);
        };
    </script>
</body>
</html>
