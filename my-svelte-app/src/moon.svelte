<script>
    
    </script>

    <div class="moon-wrapper"><div class="moon"></div></div>

    <style>
            ::global(*) {
                margin: 0;
                padding: 0;
                box-sizing: inherit;
            }
           :global( html) {
                margin: 0;
                padding: 0;
                height: 100%;
                box-sizing: border-box;
            }
            :global(body) {
                display: flex;
                align-items: center;
                justify-content: center;
                height: 600px;
                overflow: hidden;
                background-image: linear-gradient(30deg, 
            #182c51, #09101e);
            }
            .moon {
                width: 220px;
                height: 220px;
                border-radius: 50%;
                position: relative;
                background-image: linear-gradient(30deg,
                #11203d, #101c32);
                z-index: 100;
            }
            .moon-wrapper {
                position: relative;
                width: 220px;
                height: 220px;
            }
            .moon-wrapper::before {
                content: "";
                background-color: rgba(0 , 0, 0, 0);
                border-radius: 50%;
                z-index: 1;
                width: 100%;
                height: 100%;
                position: absolute;
                display: block;
                animation: eclipse-animation 3.2s linear infinite alternate;
                
            } 
        @keyframes eclipse-animation {
                0% {
                    box-shadow: none;
                    transform: translate(-30px, 30px)
                    scale(0.9); 
                }
                50% {
                    transform: translate(0px, 0px)
                    scale(1.02);
                    box-shadow: 0 0 10px #f9f0ee,
                    0 0 80px 8px #c7938b;
                    background-color: #efdbd8;
                }
                100% {
                    box-shadow: none;
                    transform: translate(30px, -30px)
                    scale(0.9);
                }

        }
        @media  (max-width: 768px){
                    .moon {
                        width: 160px;
                        height: 160px;
                    }
                }
    </style>
