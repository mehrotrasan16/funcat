# funcat
The idea is to write a command line tool that can enumerate the functions of a python(later on C,C++ and Java files) and can cat individual functions when called with the names as arguments.

syntax:
sanket@lenovo-z4070: funcat neuralnetwork.py 
    def __init__(self, n_inputs, n_hiddens_list, n_outputs, use_torch=False):
    
    def __repr__(self):
    
    def _standardizeX(self, X):
    
    def _unstandardizeX(self, Xs):
    
    def _standardizeT(self, T):
    
    def _unstandardizeT(self, Ts):
    
    def _pack(self, Vs, W):
    
    def _unpack(self, w):
    
    def _forward_pass(self, X):
    
    def _objectiveF(self, w, X, T):
    
    def _gradientF(self, w, X, T):
    
    # Another way to define dEdW without calling np.insert                        
    
    def _setup_standardize(self, X, T):
    
    def _objective_to_actual(self, objective):
    
    def train(self, X, T, n_epochs, method='scg',
    
    def use(self, X, all_outputs=False):
    
    def get_n_epochs(self):
    
    def get_error_trace(self):
    
    def get_training_time(self):
    
    def get_weight_history(self):
    
    def draw(self, input_names=None, output_names=None, gray=False):
    
    def rmse(Y, T):

sanket@lenovo-z4070: funcat neuralnetwork.py __repr__
    
        def __repr__(self):
        str = f'{type(self).__name__}({self.n_inputs}, {self.n_hiddens_list}, {self.n_outputs}, use_torch={self.use_torch})'
        if self.trained:
            str += f'\n   Network was trained for {self.n_epochs} epochs'
            str += f' that took {self.training_time:.4f} seconds. Final objective value is {self.error_trace[-1]:.3f}'
        else:
            str += '  Network is not trained.'
        return str
    
